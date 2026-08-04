\# Blueprint API



\## auth-service (8081)



| Method | Endpoint | Mô tả | Yêu cầu |

|---------|----------|-------|----------|

| POST | /auth/login | Đăng nhập | Public |

| POST | /auth/register | Đăng ký | Public |



\---



\## course-service (8082)



| Method | Endpoint | Mô tả | Quyền |

|---------|----------|-------|-------|

| GET | /courses | Danh sách môn học | Public |

| GET | /courses/{id} | Chi tiết môn học | Public |

| POST | /courses | Thêm môn học | ADMIN |

| PUT | /courses/{id} | Sửa môn học | ADMIN |

| DELETE | /courses/{id} | Xóa môn học | ADMIN |



\### Internal API



| Method | Endpoint | Mô tả |

|---------|----------|-------|

| PATCH | /internal/courses/{id}/reserve-seat | Giảm số chỗ |

| PATCH | /internal/courses/{id}/release-seat | Trả lại số chỗ |



\---



\## registration-service (8083)



| Method | Endpoint | Mô tả | Quyền |

|---------|----------|-------|-------|

| POST | /registrations | Đăng ký học phần | STUDENT |

| GET | /registrations/my | Danh sách của tôi | STUDENT |

| DELETE | /registrations/{id} | Hủy đăng ký | STUDENT / ADMIN |

