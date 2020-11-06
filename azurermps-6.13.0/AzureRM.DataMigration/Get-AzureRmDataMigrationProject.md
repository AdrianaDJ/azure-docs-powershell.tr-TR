---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591975"
---
# <span data-ttu-id="af872-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="af872-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="af872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af872-102">SYNOPSIS</span></span>
<span data-ttu-id="af872-103">Azure veritabanı geçiş projesi özelliklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="af872-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af872-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af872-104">SYNTAX</span></span>

### <span data-ttu-id="af872-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af872-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af872-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="af872-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af872-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="af872-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af872-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af872-108">DESCRIPTION</span></span>
<span data-ttu-id="af872-109">Get-AzureRmDataMigrationProject cmdlet 'i, Azure veritabanı geçiş projesi özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="af872-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="af872-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af872-110">EXAMPLES</span></span>

### <span data-ttu-id="af872-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af872-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="af872-112">Yukarıdaki örnek testresourcegroup adındaki ve testhizmeti adlı hizmet 'in altındaki test</span><span class="sxs-lookup"><span data-stu-id="af872-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="af872-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="af872-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="af872-114">Yukarıdaki örnek, gelen PSProject nesne giriş parametresine dayalı olarak Azure veritabanı geçiş projesini alır.</span><span class="sxs-lookup"><span data-stu-id="af872-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="af872-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af872-115">PARAMETERS</span></span>

### <span data-ttu-id="af872-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af872-116">-DefaultProfile</span></span>
<span data-ttu-id="af872-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af872-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af872-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af872-118">-InputObject</span></span>
<span data-ttu-id="af872-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="af872-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="af872-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="af872-120">-Name</span></span>
<span data-ttu-id="af872-121">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="af872-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af872-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af872-122">-ResourceGroupName</span></span>
<span data-ttu-id="af872-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="af872-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="af872-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="af872-124">-ResourceId</span></span>
<span data-ttu-id="af872-125">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="af872-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="af872-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="af872-126">-ServiceName</span></span>
<span data-ttu-id="af872-127">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="af872-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="af872-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af872-128">CommonParameters</span></span>
<span data-ttu-id="af872-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af872-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af872-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af872-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af872-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af872-131">INPUTS</span></span>

### <span data-ttu-id="af872-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="af872-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="af872-133">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af872-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="af872-134">System. String</span><span class="sxs-lookup"><span data-stu-id="af872-134">System.String</span></span>

## <span data-ttu-id="af872-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af872-135">OUTPUTS</span></span>

### <span data-ttu-id="af872-136">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="af872-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="af872-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af872-137">NOTES</span></span>

## <span data-ttu-id="af872-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af872-138">RELATED LINKS</span></span>
