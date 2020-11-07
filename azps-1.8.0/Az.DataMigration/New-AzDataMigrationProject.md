---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: d1f1ae44cf1b6d1b6d3afffa3e13ea34c1ffeb51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916804"
---
# <span data-ttu-id="e3030-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e3030-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="e3030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3030-102">SYNOPSIS</span></span>
<span data-ttu-id="e3030-103">Yeni bir Azure veritabanı geçiş hizmeti projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3030-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="e3030-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3030-104">SYNTAX</span></span>

### <span data-ttu-id="e3030-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3030-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3030-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="e3030-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3030-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e3030-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3030-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3030-108">DESCRIPTION</span></span>
<span data-ttu-id="e3030-109">New-AzDataMigrationProject cmdlet 'i yeni bir Azure veritabanı geçiş hizmeti projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3030-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="e3030-110">Bu cmdlet, Azure Kaynak grubu adı, yeni projenin oluşturulduğu Azure veri taşıma hizmeti 'nin adı, projenin oluşturulduğu bölge, yeni projenin benzersiz adı, kaynak ve hedef bağlantı nesneleri ve geçirilecek veritabanlarının listesi için giriş olarak hedef tür nesnesi gibi tüm gerekli parametreleri alır:.</span><span class="sxs-lookup"><span data-stu-id="e3030-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="e3030-111">Hem kaynak hem de hedef bağlantılar için yeni bir ConnectionInfo nesnesi oluşturmak için New-AzDataMigrationConnectionInfo cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e3030-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="e3030-112">Seçili veritabanları için Microsoft. Azure. Management. DataMigration. model. Databaseınfo listesi bekleniyor; Bu nesne New-AzDataMigrationDatabaseInfo cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="e3030-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="e3030-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3030-113">EXAMPLES</span></span>

### <span data-ttu-id="e3030-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3030-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="e3030-115">Yukarıdaki örnek, TestService adındaki Azure veritabanı geçiş hizmeti örneğinin altındaki Merkezi ABD bölgesinde bulunan Myvseçmsproject adlı yeni projenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3030-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="e3030-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3030-116">PARAMETERS</span></span>

### <span data-ttu-id="e3030-117">-Databaseınfo</span><span class="sxs-lookup"><span data-stu-id="e3030-117">-DatabaseInfo</span></span>
<span data-ttu-id="e3030-118">Veritabanı bilgisi.</span><span class="sxs-lookup"><span data-stu-id="e3030-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3030-119">-DefaultProfile</span></span>
<span data-ttu-id="e3030-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3030-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3030-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3030-121">-InputObject</span></span>
<span data-ttu-id="e3030-122">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e3030-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="e3030-123">-Location</span></span>
<span data-ttu-id="e3030-124">Azure veritabanı geçiş hizmeti örneğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="e3030-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="e3030-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3030-125">-Name</span></span>
<span data-ttu-id="e3030-126">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="e3030-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3030-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3030-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3030-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e3030-129">-ResourceId</span></span>
<span data-ttu-id="e3030-130">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e3030-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-131">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e3030-131">-ServiceName</span></span>
<span data-ttu-id="e3030-132">Azure veritabanı geçiş hizmeti örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3030-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="e3030-133">-SourceConnection</span></span>
<span data-ttu-id="e3030-134">Kaynak bağlantı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e3030-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e3030-135">-SourceType</span></span>
<span data-ttu-id="e3030-136">Project için kaynak platform türü.</span><span class="sxs-lookup"><span data-stu-id="e3030-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="e3030-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="e3030-137">-TargetConnection</span></span>
<span data-ttu-id="e3030-138">Hedef bağlantı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e3030-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="e3030-139">-TargetType</span></span>
<span data-ttu-id="e3030-140">Project için hedef platform türü.</span><span class="sxs-lookup"><span data-stu-id="e3030-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="e3030-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3030-141">-Confirm</span></span>
<span data-ttu-id="e3030-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3030-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3030-143">-WhatIf</span></span>
<span data-ttu-id="e3030-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3030-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3030-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3030-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3030-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3030-146">CommonParameters</span></span>
<span data-ttu-id="e3030-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3030-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3030-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3030-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3030-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3030-149">INPUTS</span></span>

### <span data-ttu-id="e3030-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e3030-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e3030-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e3030-151">System.String</span></span>

## <span data-ttu-id="e3030-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3030-152">OUTPUTS</span></span>

### <span data-ttu-id="e3030-153">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="e3030-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="e3030-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3030-154">NOTES</span></span>

## <span data-ttu-id="e3030-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3030-155">RELATED LINKS</span></span>
