🇧🇷 Opencart Delete Sessions
=======================

Simples comando para executar SQL para limpeza de sessões expiradas do banco de dados.

Remova registros com mais de 1 dia
DELETE FROM `oc_session` WHERE TIMESTAMPADD(DAY, 1, expire) < NOW();

Remova registros com mais de 1 hora
DELETE FROM `oc_session` WHERE TIMESTAMPADD(HOUR, 1, expire) < NOW();
