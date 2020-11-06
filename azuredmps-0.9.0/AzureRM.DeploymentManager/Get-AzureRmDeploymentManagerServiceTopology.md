---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572445"
---
# <span data-ttu-id="bd522-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd522-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="bd522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd522-102">SYNOPSIS</span></span>
<span data-ttu-id="bd522-103">Hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="bd522-103">Gets a service topology.</span></span>

## <span data-ttu-id="bd522-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd522-104">SYNTAX</span></span>

### <span data-ttu-id="bd522-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd522-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd522-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bd522-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd522-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd522-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd522-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd522-108">DESCRIPTION</span></span>
<span data-ttu-id="bd522-109">**Get-AzureRmDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="bd522-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="bd522-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerServiceTopology cmdlet 'ini kullanarak topolojiye değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd522-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="bd522-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="bd522-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="bd522-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd522-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="bd522-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd522-113">EXAMPLES</span></span>

### <span data-ttu-id="bd522-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd522-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="bd522-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bd522-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd522-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="bd522-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="bd522-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bd522-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd522-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini alma.</span><span class="sxs-lookup"><span data-stu-id="bd522-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="bd522-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini alır.</span><span class="sxs-lookup"><span data-stu-id="bd522-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="bd522-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd522-120">PARAMETERS</span></span>

### <span data-ttu-id="bd522-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd522-121">-DefaultProfile</span></span>
<span data-ttu-id="bd522-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd522-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd522-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd522-123">-Name</span></span>
<span data-ttu-id="bd522-124">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="bd522-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="bd522-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd522-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd522-126">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bd522-126">The resource group.</span></span>

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

### <span data-ttu-id="bd522-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bd522-127">-ResourceId</span></span>
<span data-ttu-id="bd522-128">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bd522-128">The resource identifier.</span></span>

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

### <span data-ttu-id="bd522-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd522-129">-ServiceTopology</span></span>
<span data-ttu-id="bd522-130">Hizmet topolojisi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bd522-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="bd522-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd522-131">CommonParameters</span></span>
<span data-ttu-id="bd522-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd522-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd522-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd522-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd522-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd522-134">INPUTS</span></span>

### <span data-ttu-id="bd522-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bd522-135">None</span></span>

## <span data-ttu-id="bd522-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd522-136">OUTPUTS</span></span>

### <span data-ttu-id="bd522-137">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="bd522-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="bd522-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd522-138">NOTES</span></span>

## <span data-ttu-id="bd522-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd522-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd522-140">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd522-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="bd522-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd522-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="bd522-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bd522-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)