---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761782"
---
# <span data-ttu-id="b0905-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b0905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0905-102">SYNOPSIS</span></span>
<span data-ttu-id="b0905-103">Bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="b0905-103">Gets an artifact source.</span></span>

## <span data-ttu-id="b0905-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0905-104">SYNTAX</span></span>

### <span data-ttu-id="b0905-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0905-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0905-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b0905-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0905-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0905-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0905-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0905-108">DESCRIPTION</span></span>
<span data-ttu-id="b0905-109">**Get-AzureRmDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağı alır ve bu yapıt kaynağını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b0905-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="b0905-110">Yapıt kaynağını adına ve kaynak grup adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="b0905-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="b0905-111">Alternatif olarak, ArtifactSource nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0905-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="b0905-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerArtifactSource cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0905-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="b0905-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0905-113">EXAMPLES</span></span>

### <span data-ttu-id="b0905-114">Örnek 1: yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="b0905-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="b0905-115">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="b0905-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b0905-116">Örnek 2: kaynak tanımlayıcısını kullanarak yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="b0905-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="b0905-117">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="b0905-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b0905-118">Örnek 3: New-AzureRmDeploymentManagerArtifactSource tarafından döndürülen bir nesneyi kullanarak yapıt kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="b0905-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="b0905-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="b0905-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="b0905-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0905-120">PARAMETERS</span></span>

### <span data-ttu-id="b0905-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-121">-ArtifactSource</span></span>
<span data-ttu-id="b0905-122">Yapıt kaynağı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b0905-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="b0905-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0905-123">-DefaultProfile</span></span>
<span data-ttu-id="b0905-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0905-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0905-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0905-125">-Name</span></span>
<span data-ttu-id="b0905-126">Yapıt kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="b0905-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0905-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0905-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0905-128">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b0905-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0905-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b0905-129">-ResourceId</span></span>
<span data-ttu-id="b0905-130">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b0905-130">The resource identifier.</span></span>

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

### <span data-ttu-id="b0905-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0905-131">CommonParameters</span></span>
<span data-ttu-id="b0905-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0905-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0905-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0905-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0905-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0905-134">INPUTS</span></span>

### <span data-ttu-id="b0905-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b0905-135">None</span></span>

## <span data-ttu-id="b0905-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0905-136">OUTPUTS</span></span>

### <span data-ttu-id="b0905-137">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b0905-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0905-138">NOTES</span></span>

## <span data-ttu-id="b0905-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0905-139">RELATED LINKS</span></span>

[<span data-ttu-id="b0905-140">Yeni-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="b0905-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="b0905-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0905-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)