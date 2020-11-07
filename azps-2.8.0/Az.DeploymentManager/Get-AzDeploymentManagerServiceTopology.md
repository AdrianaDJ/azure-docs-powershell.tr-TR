---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752144"
---
# <span data-ttu-id="fd72a-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fd72a-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fd72a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd72a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd72a-103">Hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="fd72a-103">Gets the service topology.</span></span>

## <span data-ttu-id="fd72a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd72a-104">SYNTAX</span></span>

### <span data-ttu-id="fd72a-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd72a-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd72a-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fd72a-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd72a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd72a-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd72a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd72a-108">DESCRIPTION</span></span>
<span data-ttu-id="fd72a-109">**Get-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="fd72a-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="fd72a-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerServiceTopology cmdlet 'ini kullanarak topolojiye değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd72a-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="fd72a-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="fd72a-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="fd72a-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd72a-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="fd72a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd72a-113">EXAMPLES</span></span>

### <span data-ttu-id="fd72a-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd72a-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="fd72a-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fd72a-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fd72a-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="fd72a-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="fd72a-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fd72a-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fd72a-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="fd72a-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fd72a-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="fd72a-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="fd72a-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd72a-120">PARAMETERS</span></span>

### <span data-ttu-id="fd72a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd72a-121">-DefaultProfile</span></span>
<span data-ttu-id="fd72a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd72a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd72a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd72a-123">-InputObject</span></span>
<span data-ttu-id="fd72a-124">Hizmet topolojisi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fd72a-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="fd72a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd72a-125">-Name</span></span>
<span data-ttu-id="fd72a-126">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="fd72a-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd72a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd72a-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd72a-128">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fd72a-128">The resource group.</span></span>

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

### <span data-ttu-id="fd72a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fd72a-129">-ResourceId</span></span>
<span data-ttu-id="fd72a-130">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fd72a-130">The resource identifier.</span></span>

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

### <span data-ttu-id="fd72a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd72a-131">CommonParameters</span></span>
<span data-ttu-id="fd72a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd72a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd72a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd72a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd72a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd72a-134">INPUTS</span></span>

### <span data-ttu-id="fd72a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fd72a-135">System.String</span></span>

### <span data-ttu-id="fd72a-136">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fd72a-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fd72a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd72a-137">OUTPUTS</span></span>

### <span data-ttu-id="fd72a-138">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fd72a-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fd72a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd72a-139">NOTES</span></span>

## <span data-ttu-id="fd72a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd72a-140">RELATED LINKS</span></span>
