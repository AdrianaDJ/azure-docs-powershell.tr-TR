---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: fc400c9eeb64acfa081d5a60a5e65089f415817b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764139"
---
# <span data-ttu-id="7d459-101">New-AzureRmDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="7d459-101">New-AzureRmDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="7d459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d459-102">SYNOPSIS</span></span>
<span data-ttu-id="7d459-103">Geçiş görevi için kullanılacak eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d459-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d459-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d459-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String>
 -TableMap <Hashtable> [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>]
 [-TargetSetting <Hashtable>] -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d459-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d459-105">DESCRIPTION</span></span>

<span data-ttu-id="7d459-106">New-AzureRmDataMigrationSyncSelectedDB cmdlet 'i, kaynak ve hedef veritabanları hakkında bilgi içeren eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d459-106">The New-AzureRmDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="7d459-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d459-107">EXAMPLES</span></span>

### <span data-ttu-id="7d459-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7d459-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzureRmDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="7d459-109">Bu örnek, veritabanı $DatabaseName $DatabaseName geçiş ayarlarını açıklayan bir veritabanı meta veri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d459-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="7d459-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d459-110">PARAMETERS</span></span>

### <span data-ttu-id="7d459-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d459-111">-DefaultProfile</span></span>
<span data-ttu-id="7d459-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d459-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d459-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="7d459-113">-MigrationSetting</span></span>
<span data-ttu-id="7d459-114">Geçiş davranışını ayarlamaya yönelik geçiş ayarları</span><span class="sxs-lookup"><span data-stu-id="7d459-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7d459-115">-SchemaName</span></span>
<span data-ttu-id="7d459-116">Geçirilecek şema adı</span><span class="sxs-lookup"><span data-stu-id="7d459-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="7d459-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d459-117">-SourceDatabaseName</span></span>
<span data-ttu-id="7d459-118">Kaynak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="7d459-118">The name of the source database.</span></span>

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

### <span data-ttu-id="7d459-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="7d459-119">-SourceSetting</span></span>
<span data-ttu-id="7d459-120">Kaynak uç noktası geçiş davranışını ayarlamak için kaynak ayarlar</span><span class="sxs-lookup"><span data-stu-id="7d459-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="7d459-121">-TableMap</span></span>
<span data-ttu-id="7d459-122">Kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="7d459-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d459-123">-TargetDatabaseName</span></span>
<span data-ttu-id="7d459-124">Hedef veritabanının adı</span><span class="sxs-lookup"><span data-stu-id="7d459-124">The name of the target database</span></span>

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

### <span data-ttu-id="7d459-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="7d459-125">-TargetSetting</span></span>
<span data-ttu-id="7d459-126">Hedef uç nokta geçiş davranışını ayarlamak için hedef ayarlar</span><span class="sxs-lookup"><span data-stu-id="7d459-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d459-127">CommonParameters</span></span>
<span data-ttu-id="7d459-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d459-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d459-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d459-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d459-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d459-130">INPUTS</span></span>

### <span data-ttu-id="7d459-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7d459-131">None</span></span>

## <span data-ttu-id="7d459-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d459-132">OUTPUTS</span></span>

### <span data-ttu-id="7d459-133">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbsynctaskınput</span><span class="sxs-lookup"><span data-stu-id="7d459-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="7d459-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d459-134">NOTES</span></span>

## <span data-ttu-id="7d459-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d459-135">RELATED LINKS</span></span>
