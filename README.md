# Mousegoing

mic testing
Testing 2


need this NOW.

koi code do bhai...

 def call(self, func, *args, **kwargs):
        current_state = self._check_state()
        if current_state == False:
            return
        try:
            now = datetime.utcnow()
            if now >= (self._opened_since + self._reset_timeout):
                func(*args, **kwargs)
            else:
                self._on_failure()
                return
        except Exception as e:
