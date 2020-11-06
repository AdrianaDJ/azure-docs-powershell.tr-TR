---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594086"
---
# <span data-ttu-id="60ca1-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="60ca1-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="60ca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="60ca1-103">Yeni bir Azure veritabanı geçiş hizmeti projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60ca1-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ca1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60ca1-104">SYNTAX</span></span>

### <span data-ttu-id="60ca1-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60ca1-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="60ca1-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="60ca1-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="60ca1-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="60ca1-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="60ca1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60ca1-108">DESCRIPTION</span></span>
<span data-ttu-id="60ca1-109">New-AzureRmDataMigrationProject cmdlet 'i yeni bir Azure veritabanı geçiş hizmeti projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60ca1-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="60ca1-110">Bu cmdlet, Azure Kaynak grubu adı, yeni projenin oluşturulduğu Azure veri taşıma hizmeti 'nin adı, projenin oluşturulduğu bölge, yeni projenin benzersiz adı, kaynak ve hedef bağlantı nesneleri ve geçirilecek veritabanlarının listesi için giriş olarak hedef tür nesnesi gibi tüm gerekli parametreleri alır:.</span><span class="sxs-lookup"><span data-stu-id="60ca1-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="60ca1-111">Hem kaynak hem de hedef bağlantılar için yeni bir ConnectionInfo nesnesi oluşturmak için New-AzureRmDataMigrationConnectionInfo cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="60ca1-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="60ca1-112">Seçili veritabanları için Microsoft. Azure. Management. DataMigration. model. Databaseınfo listesi bekleniyor; Bu nesne New-AzureRmDataMigrationDatabaseInfo cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="60ca1-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="60ca1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60ca1-113">EXAMPLES</span></span>

### <span data-ttu-id="60ca1-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60ca1-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="60ca1-115">Yukarıdaki örnek, TestService adındaki Azure veritabanı geçiş hizmeti örneğinin altındaki Merkezi ABD bölgesinde bulunan Myvseçmsproject adlı yeni projenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="60ca1-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="60ca1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60ca1-116">PARAMETERS</span></span>

### <span data-ttu-id="60ca1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="60ca1-117">-Confirm</span></span>
<span data-ttu-id="60ca1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60ca1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-119">-Databaseınfo []</span><span class="sxs-lookup"><span data-stu-id="60ca1-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="60ca1-120">Veritabanı bilgileri</span><span class="sxs-lookup"><span data-stu-id="60ca1-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ca1-121">-DefaultProfile</span></span>
<span data-ttu-id="60ca1-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60ca1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="60ca1-123">-Location</span></span>
<span data-ttu-id="60ca1-124">Azure veritabanı geçiş hizmeti örneğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="60ca1-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="60ca1-125">-ProjectName</span></span>
<span data-ttu-id="60ca1-126">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="60ca1-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ca1-127">-ResourceGroupName</span></span>
<span data-ttu-id="60ca1-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="60ca1-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="60ca1-129">-ServiceName</span></span>
<span data-ttu-id="60ca1-130">Azure veritabanı geçiş hizmeti örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="60ca1-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="60ca1-131">-SourceConnection</span></span>
<span data-ttu-id="60ca1-132">Kaynak bağlantı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="60ca1-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="60ca1-133">-SourceType</span></span>
<span data-ttu-id="60ca1-134">Project için kaynak platform türü.</span><span class="sxs-lookup"><span data-stu-id="60ca1-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="60ca1-135">-TargetConnection</span></span>
<span data-ttu-id="60ca1-136">Hedef bağlantı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="60ca1-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="60ca1-137">-TargetType</span></span>
<span data-ttu-id="60ca1-138">Project için hedef platform türü.</span><span class="sxs-lookup"><span data-stu-id="60ca1-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="60ca1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60ca1-139">OUTPUTS</span></span>

### <span data-ttu-id="60ca1-140">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="60ca1-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="60ca1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60ca1-141">NOTES</span></span>

## <span data-ttu-id="60ca1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60ca1-142">RELATED LINKS</span></span>

