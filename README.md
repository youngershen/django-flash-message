#django-flash-message

usage:

    set the DJANGO_FLASH_MESSAGE_STORAGE in settings.py
    DJANGO_FLASH_MESSAGE_STORAGE = 'session'
    or
    DJANGO_FLASH_MESSAGE_STORAGE = 'cookie'
    save the message in session or cookie

    in your views
    from django_flash_message.storage import storage
    storage.add_message(request, 'error', 'invalid email or password')
    storage.get_message(request, 'error')

    all messages are single use , so i call it the flash message