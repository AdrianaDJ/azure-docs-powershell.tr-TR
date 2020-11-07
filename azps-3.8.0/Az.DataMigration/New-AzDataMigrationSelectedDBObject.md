---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937382"
---
# <span data-ttu-id="35c76-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="35c76-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="35c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35c76-102">SYNOPSIS</span></span>
<span data-ttu-id="35c76-103">Geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı giriş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35c76-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="35c76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35c76-104">SYNTAX</span></span>

### <span data-ttu-id="35c76-105">MigrateSqlServerSqlDb (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35c76-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c76-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="35c76-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35c76-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35c76-107">DESCRIPTION</span></span>
<span data-ttu-id="35c76-108">New-AzDataMigrationSelectedDB cmdlet 'i, geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı bilgi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35c76-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="35c76-109">Bu cmdlet, New-AzDataMigrationTask cmdlet 'ini içeren bir parametre olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="35c76-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="35c76-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35c76-110">EXAMPLES</span></span>

### <span data-ttu-id="35c76-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35c76-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="35c76-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="35c76-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="35c76-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35c76-113">PARAMETERS</span></span>

### <span data-ttu-id="35c76-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="35c76-114">-BackupFileShare</span></span>
<span data-ttu-id="35c76-115">Bu veritabanının kaynak sunucusu veritabanı dosyalarının yedeklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="35c76-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="35c76-116">Her veritabanı için dosya paylaşımı bilgilerini geçersiz kılmak için bu ayarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="35c76-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="35c76-117">Sunucu için tam nitelikli etki alanı adı kullanın.</span><span class="sxs-lookup"><span data-stu-id="35c76-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="35c76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c76-118">-DefaultProfile</span></span>
<span data-ttu-id="35c76-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35c76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c76-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="35c76-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="35c76-121">Geçiş yapmadan önce veritabanını ReadOnly olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="35c76-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="35c76-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="35c76-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="35c76-123">Geçiş türünü SQL Server 'a SQL DB geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="35c76-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="35c76-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="35c76-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="35c76-125">Geçiş türünü SQL Server 'a SQL DB MI geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="35c76-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="35c76-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="35c76-126">-SourceDatabaseName</span></span>
<span data-ttu-id="35c76-127">Kaynak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="35c76-127">The name of the source database.</span></span>

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

### <span data-ttu-id="35c76-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="35c76-128">-TableMap</span></span>
<span data-ttu-id="35c76-129">kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="35c76-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="35c76-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="35c76-130">-TargetDatabaseName</span></span>
<span data-ttu-id="35c76-131">Hedef veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="35c76-131">The name of the target database.</span></span>

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

### <span data-ttu-id="35c76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c76-132">CommonParameters</span></span>
<span data-ttu-id="35c76-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35c76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c76-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c76-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c76-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35c76-135">INPUTS</span></span>

### <span data-ttu-id="35c76-136">Microsoft. Azure. Management. DataMigration. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="35c76-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="35c76-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35c76-137">OUTPUTS</span></span>

### <span data-ttu-id="35c76-138">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="35c76-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="35c76-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35c76-139">NOTES</span></span>

## <span data-ttu-id="35c76-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35c76-140">RELATED LINKS</span></span>
