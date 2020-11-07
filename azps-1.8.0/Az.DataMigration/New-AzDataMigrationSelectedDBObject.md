---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 502e64ba553f20983bd437fea40d5247cf04548f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761029"
---
# <span data-ttu-id="21b88-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="21b88-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="21b88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21b88-102">SYNOPSIS</span></span>
<span data-ttu-id="21b88-103">Geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı giriş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21b88-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="21b88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21b88-104">SYNTAX</span></span>

### <span data-ttu-id="21b88-105">MigrateSqlServerSqlDb (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21b88-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21b88-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="21b88-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21b88-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="21b88-107">DESCRIPTION</span></span>
<span data-ttu-id="21b88-108">New-AzDataMigrationSelectedDB cmdlet 'i, geçiş için kaynak ve hedef veritabanları hakkında bilgi içeren bir veritabanı bilgi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21b88-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="21b88-109">Bu cmdlet, New-AzDataMigrationTask cmdlet 'ini içeren bir parametre olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="21b88-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="21b88-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21b88-110">EXAMPLES</span></span>

### <span data-ttu-id="21b88-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21b88-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="21b88-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="21b88-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="21b88-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21b88-113">PARAMETERS</span></span>

### <span data-ttu-id="21b88-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="21b88-114">-BackupFileShare</span></span>
<span data-ttu-id="21b88-115">Bu veritabanının kaynak sunucusu veritabanı dosyalarının yedeklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="21b88-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="21b88-116">Her veritabanı için dosya paylaşımı bilgilerini geçersiz kılmak için bu ayarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="21b88-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="21b88-117">Sunucu için tam nitelikli etki alanı adı kullanın.</span><span class="sxs-lookup"><span data-stu-id="21b88-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="21b88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b88-118">-DefaultProfile</span></span>
<span data-ttu-id="21b88-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21b88-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21b88-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="21b88-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="21b88-121">Geçiş yapmadan önce veritabanını ReadOnly olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="21b88-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="21b88-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="21b88-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="21b88-123">Geçiş türünü SQL Server 'a SQL DB geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="21b88-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="21b88-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="21b88-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="21b88-125">Geçiş türünü SQL Server 'a SQL DB MI geçişine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="21b88-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="21b88-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="21b88-126">-SourceDatabaseName</span></span>
<span data-ttu-id="21b88-127">Kaynak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="21b88-127">The name of the source database.</span></span>

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

### <span data-ttu-id="21b88-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="21b88-128">-TableMap</span></span>
<span data-ttu-id="21b88-129">kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="21b88-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="21b88-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="21b88-130">-TargetDatabaseName</span></span>
<span data-ttu-id="21b88-131">Hedef veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="21b88-131">The name of the target database.</span></span>

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

### <span data-ttu-id="21b88-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b88-132">CommonParameters</span></span>
<span data-ttu-id="21b88-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21b88-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b88-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b88-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b88-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21b88-135">INPUTS</span></span>

### <span data-ttu-id="21b88-136">Microsoft. Azure. Management. DataMigration. modeller. FileShare</span><span class="sxs-lookup"><span data-stu-id="21b88-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="21b88-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21b88-137">OUTPUTS</span></span>

### <span data-ttu-id="21b88-138">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="21b88-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="21b88-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21b88-139">NOTES</span></span>

## <span data-ttu-id="21b88-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21b88-140">RELATED LINKS</span></span>
