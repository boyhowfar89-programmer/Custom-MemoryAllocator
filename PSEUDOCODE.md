FUNCTION sage_malloc(requested_size):

    IF requested_size == 0:
        RETURN NULL

    used_bytes =
        next_free_byte - memory_pool

    bytes_remaining =
        POOL_SIZE - used_bytes

    IF requested_size > bytes_remaining:
        RETURN NULL

    allocation_start =
        next_free_byte

    next_free_byte =
        next_free_byte + requested_size

    RETURN allocation_start
