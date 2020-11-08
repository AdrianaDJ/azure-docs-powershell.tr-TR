---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104389"
---
# <span data-ttu-id="62ee4-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="62ee4-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="62ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="62ee4-103">Hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="62ee4-103">Gets the service unit.</span></span>

## <span data-ttu-id="62ee4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62ee4-104">SYNTAX</span></span>

### <span data-ttu-id="62ee4-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62ee4-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ee4-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="62ee4-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ee4-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="62ee4-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ee4-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="62ee4-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62ee4-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="62ee4-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ee4-110">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="62ee4-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62ee4-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="62ee4-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ee4-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="62ee4-112">DESCRIPTION</span></span>
<span data-ttu-id="62ee4-113">**Get-AzDeploymentManagerServiceUnit** cmdlet 'i, bir hizmette hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="62ee4-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="62ee4-114">Hizmet birimini adına, tanımladığı hizmete, hizmet topolojisi adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="62ee4-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="62ee4-115">Alternatif olarak, ServiceUnit nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62ee4-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="62ee4-116">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerServiceUnit cmdlet 'ini kullanarak hizmet birimine değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62ee4-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="62ee4-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62ee4-117">EXAMPLES</span></span>

### <span data-ttu-id="62ee4-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62ee4-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="62ee4-119">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62ee4-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="62ee4-120">Örnek 2: kaynak tanımlayıcısını kullanarak bir hizmet birimi alın.</span><span class="sxs-lookup"><span data-stu-id="62ee4-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="62ee4-121">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62ee4-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="62ee4-122">Örnek 3: hizmet birimi nesnesini kullanarak bir hizmet birimi alın.</span><span class="sxs-lookup"><span data-stu-id="62ee4-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="62ee4-123">Bu komut, adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="62ee4-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="62ee4-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62ee4-124">PARAMETERS</span></span>

### <span data-ttu-id="62ee4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ee4-125">-DefaultProfile</span></span>
<span data-ttu-id="62ee4-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62ee4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62ee4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62ee4-127">-InputObject</span></span>
<span data-ttu-id="62ee4-128">Hizmet birimi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="62ee4-128">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="62ee4-129">-Name</span></span>
<span data-ttu-id="62ee4-130">Hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ee4-131">-ResourceGroupName</span></span>
<span data-ttu-id="62ee4-132">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="62ee4-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="62ee4-133">-ResourceId</span></span>
<span data-ttu-id="62ee4-134">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-134">The resource identifier.</span></span>

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

### <span data-ttu-id="62ee4-135">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="62ee4-135">-ServiceName</span></span>
<span data-ttu-id="62ee4-136">Hizmet biriminin parçası olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="62ee4-137">-ServiceObject</span></span>
<span data-ttu-id="62ee4-138">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="62ee4-138">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="62ee4-139">-ServiceResourceId</span></span>
<span data-ttu-id="62ee4-140">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-140">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="62ee4-141">-ServiceTopologyName</span></span>
<span data-ttu-id="62ee4-142">Hizmet biriminin parçası olan hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="62ee4-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="62ee4-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="62ee4-144">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="62ee4-144">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-145">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="62ee4-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="62ee4-146">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="62ee4-146">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ee4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ee4-147">CommonParameters</span></span>
<span data-ttu-id="62ee4-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62ee4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ee4-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62ee4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ee4-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62ee4-150">INPUTS</span></span>

### <span data-ttu-id="62ee4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="62ee4-151">System.String</span></span>

### <span data-ttu-id="62ee4-152">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="62ee4-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="62ee4-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62ee4-153">OUTPUTS</span></span>

### <span data-ttu-id="62ee4-154">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="62ee4-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="62ee4-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62ee4-155">NOTES</span></span>

## <span data-ttu-id="62ee4-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62ee4-156">RELATED LINKS</span></span>
