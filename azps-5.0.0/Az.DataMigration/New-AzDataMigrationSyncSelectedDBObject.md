---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320405"
---
# <span data-ttu-id="e3156-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e3156-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="e3156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3156-102">SYNOPSIS</span></span>
<span data-ttu-id="e3156-103">Geçiş görevi için kullanılacak eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3156-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="e3156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3156-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3156-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3156-105">DESCRIPTION</span></span>

<span data-ttu-id="e3156-106">New-AzDataMigrationSyncSelectedDB cmdlet 'i, kaynak ve hedef veritabanları hakkında bilgi içeren eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3156-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="e3156-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3156-107">EXAMPLES</span></span>

### <span data-ttu-id="e3156-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3156-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="e3156-109">Bu örnek, veritabanı $DatabaseName $DatabaseName geçiş ayarlarını açıklayan bir veritabanı meta veri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3156-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="e3156-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3156-110">PARAMETERS</span></span>

### <span data-ttu-id="e3156-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3156-111">-DefaultProfile</span></span>
<span data-ttu-id="e3156-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3156-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3156-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="e3156-113">-MigrationSetting</span></span>
<span data-ttu-id="e3156-114">Geçiş davranışını ayarlamaya yönelik geçiş ayarları</span><span class="sxs-lookup"><span data-stu-id="e3156-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="e3156-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e3156-115">-SchemaName</span></span>
<span data-ttu-id="e3156-116">Geçirilecek şema adı</span><span class="sxs-lookup"><span data-stu-id="e3156-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="e3156-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3156-117">-SourceDatabaseName</span></span>
<span data-ttu-id="e3156-118">Kaynak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e3156-118">The name of the source database.</span></span>

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

### <span data-ttu-id="e3156-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="e3156-119">-SourceSetting</span></span>
<span data-ttu-id="e3156-120">Kaynak uç noktası geçiş davranışını ayarlamak için kaynak ayarlar</span><span class="sxs-lookup"><span data-stu-id="e3156-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="e3156-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="e3156-121">-TableMap</span></span>
<span data-ttu-id="e3156-122">Kaynak hedef tablolarla eşleme</span><span class="sxs-lookup"><span data-stu-id="e3156-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="e3156-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3156-123">-TargetDatabaseName</span></span>
<span data-ttu-id="e3156-124">Hedef veritabanının adı</span><span class="sxs-lookup"><span data-stu-id="e3156-124">The name of the target database</span></span>

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

### <span data-ttu-id="e3156-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="e3156-125">-TargetSetting</span></span>
<span data-ttu-id="e3156-126">Hedef uç nokta geçiş davranışını ayarlamak için hedef ayarlar</span><span class="sxs-lookup"><span data-stu-id="e3156-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="e3156-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3156-127">CommonParameters</span></span>
<span data-ttu-id="e3156-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3156-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3156-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3156-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3156-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3156-130">INPUTS</span></span>

### <span data-ttu-id="e3156-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e3156-131">None</span></span>

## <span data-ttu-id="e3156-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3156-132">OUTPUTS</span></span>

### <span data-ttu-id="e3156-133">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbsynctaskınput</span><span class="sxs-lookup"><span data-stu-id="e3156-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="e3156-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3156-134">NOTES</span></span>

## <span data-ttu-id="e3156-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3156-135">RELATED LINKS</span></span>
