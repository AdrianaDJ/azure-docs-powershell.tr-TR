---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104406"
---
# <span data-ttu-id="fd9f0-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="fd9f0-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="fd9f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd9f0-102">SYNOPSIS</span></span>

<span data-ttu-id="fd9f0-103">Yapıt kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="fd9f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd9f0-104">SYNTAX</span></span>

### <span data-ttu-id="fd9f0-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd9f0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd9f0-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fd9f0-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd9f0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd9f0-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd9f0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd9f0-108">DESCRIPTION</span></span>
<span data-ttu-id="fd9f0-109">**Get-AzDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağı alır ve bu yapıt kaynağını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="fd9f0-110">Yapıt kaynağını adına ve kaynak grup adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="fd9f0-111">Alternatif olarak, ArtifactSource nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="fd9f0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd9f0-112">EXAMPLES</span></span>

### <span data-ttu-id="fd9f0-113">Örnek 1: yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="fd9f0-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="fd9f0-114">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fd9f0-115">Örnek 2: kaynak tanımlayıcısını kullanarak yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="fd9f0-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="fd9f0-116">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fd9f0-117">Örnek 3: New-AzDeploymentManagerArtifactSource tarafından döndürülen bir nesneyi kullanarak yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="fd9f0-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="fd9f0-118">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="fd9f0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd9f0-119">PARAMETERS</span></span>

### <span data-ttu-id="fd9f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9f0-120">-DefaultProfile</span></span>
<span data-ttu-id="fd9f0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd9f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd9f0-122">-InputObject</span></span>
<span data-ttu-id="fd9f0-123">Yapıt kaynağı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-123">Artifact Source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f0-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd9f0-124">-Name</span></span>
<span data-ttu-id="fd9f0-125">Yapıt kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd9f0-127">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f0-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fd9f0-128">-ResourceId</span></span>
<span data-ttu-id="fd9f0-129">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-129">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9f0-130">CommonParameters</span></span>
<span data-ttu-id="fd9f0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9f0-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd9f0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9f0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd9f0-133">INPUTS</span></span>

### <span data-ttu-id="fd9f0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fd9f0-134">System.String</span></span>

### <span data-ttu-id="fd9f0-135">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="fd9f0-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="fd9f0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd9f0-136">OUTPUTS</span></span>

### <span data-ttu-id="fd9f0-137">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="fd9f0-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="fd9f0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd9f0-138">NOTES</span></span>

## <span data-ttu-id="fd9f0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd9f0-139">RELATED LINKS</span></span>
