---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108327"
---
# <span data-ttu-id="151bf-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="151bf-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="151bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="151bf-102">SYNOPSIS</span></span>
<span data-ttu-id="151bf-103">Hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="151bf-103">Gets the service topology.</span></span>

## <span data-ttu-id="151bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="151bf-104">SYNTAX</span></span>

### <span data-ttu-id="151bf-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="151bf-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="151bf-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="151bf-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="151bf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="151bf-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="151bf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="151bf-108">DESCRIPTION</span></span>
<span data-ttu-id="151bf-109">**Get-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="151bf-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="151bf-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerServiceTopology cmdlet 'ini kullanarak topolojiye değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="151bf-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="151bf-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="151bf-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="151bf-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="151bf-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="151bf-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="151bf-113">EXAMPLES</span></span>

### <span data-ttu-id="151bf-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="151bf-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="151bf-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="151bf-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="151bf-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="151bf-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="151bf-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="151bf-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="151bf-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="151bf-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="151bf-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="151bf-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="151bf-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="151bf-120">PARAMETERS</span></span>

### <span data-ttu-id="151bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151bf-121">-DefaultProfile</span></span>
<span data-ttu-id="151bf-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="151bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="151bf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="151bf-123">-InputObject</span></span>
<span data-ttu-id="151bf-124">Hizmet topolojisi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="151bf-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="151bf-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="151bf-125">-Name</span></span>
<span data-ttu-id="151bf-126">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="151bf-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="151bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="151bf-128">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="151bf-128">The resource group.</span></span>

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

### <span data-ttu-id="151bf-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="151bf-129">-ResourceId</span></span>
<span data-ttu-id="151bf-130">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="151bf-130">The resource identifier.</span></span>

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

### <span data-ttu-id="151bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151bf-131">CommonParameters</span></span>
<span data-ttu-id="151bf-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="151bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151bf-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="151bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151bf-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="151bf-134">INPUTS</span></span>

### <span data-ttu-id="151bf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="151bf-135">System.String</span></span>

### <span data-ttu-id="151bf-136">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="151bf-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="151bf-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="151bf-137">OUTPUTS</span></span>

### <span data-ttu-id="151bf-138">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="151bf-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="151bf-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="151bf-139">NOTES</span></span>

## <span data-ttu-id="151bf-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="151bf-140">RELATED LINKS</span></span>
