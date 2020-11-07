---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762110"
---
# <span data-ttu-id="52718-101">New-AzureRmDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="52718-101">New-AzureRmDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="52718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52718-102">SYNOPSIS</span></span>
<span data-ttu-id="52718-103">Geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı giriş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52718-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52718-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52718-104">SYNTAX</span></span>

### <span data-ttu-id="52718-105">MigrateSqlServerSqlDb (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52718-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52718-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="52718-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52718-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52718-107">DESCRIPTION</span></span>
<span data-ttu-id="52718-108">New-AzureRmDataMigrationSelectedDB cmdlet 'i, geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı bilgi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52718-108">The New-AzureRmDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="52718-109">Bu cmdlet, New-AzureRmDataMigrationTask cmdlet 'ini içeren bir parametre olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="52718-109">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="52718-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52718-110">EXAMPLES</span></span>

### <span data-ttu-id="52718-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52718-111">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### <span data-ttu-id="52718-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="52718-112">Example 2</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## <span data-ttu-id="52718-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52718-113">PARAMETERS</span></span>

### <span data-ttu-id="52718-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="52718-114">-BackupFileShare</span></span>
<span data-ttu-id="52718-115">Bu veritabanının kaynak sunucusu veritabanı dosyalarının yedeklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="52718-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="52718-116">Her veritabanı için dosya paylaşımı bilgilerini geçersiz kılmak için bu ayarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="52718-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="52718-117">Sunucu için tam nitelikli etki alanı adı kullanın.</span><span class="sxs-lookup"><span data-stu-id="52718-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52718-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52718-118">-DefaultProfile</span></span>
<span data-ttu-id="52718-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52718-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="52718-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="52718-121">Geçiş yapmadan önce veritabanını ReadOnly olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="52718-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="52718-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="52718-123">Geçiş türünü SQL Server 'a SQL DB geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52718-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="52718-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="52718-125">Geçiş türünü SQL Server 'a SQL DB MI geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52718-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="52718-126">-SourceDatabaseName</span></span>
<span data-ttu-id="52718-127">Kaynak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="52718-127">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="52718-128">-TableMap</span></span>
<span data-ttu-id="52718-129">kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="52718-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="52718-130">-TargetDatabaseName</span></span>
<span data-ttu-id="52718-131">Hedef veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="52718-131">The name of the target database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52718-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52718-132">CommonParameters</span></span>
<span data-ttu-id="52718-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52718-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52718-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52718-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52718-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52718-135">INPUTS</span></span>

### <span data-ttu-id="52718-136">Microsoft. Azure. Management. DataMigration. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="52718-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="52718-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52718-137">OUTPUTS</span></span>

### <span data-ttu-id="52718-138">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="52718-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="52718-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52718-139">NOTES</span></span>

## <span data-ttu-id="52718-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52718-140">RELATED LINKS</span></span>
