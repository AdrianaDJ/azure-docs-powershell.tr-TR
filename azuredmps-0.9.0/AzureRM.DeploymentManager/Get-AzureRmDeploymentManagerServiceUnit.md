---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761705"
---
# <span data-ttu-id="67a76-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="67a76-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="67a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a76-102">SYNOPSIS</span></span>
<span data-ttu-id="67a76-103">Hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="67a76-103">Gets a service unit.</span></span>

## <span data-ttu-id="67a76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67a76-104">SYNTAX</span></span>

### <span data-ttu-id="67a76-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67a76-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a76-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="67a76-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a76-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="67a76-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a76-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="67a76-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a76-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="67a76-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a76-110">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="67a76-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67a76-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="67a76-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a76-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="67a76-112">DESCRIPTION</span></span>
<span data-ttu-id="67a76-113">**Get-AzureRmDeploymentManagerServiceUnit** cmdlet 'i, bir hizmette hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="67a76-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="67a76-114">Hizmet birimini adına, tanımladığı hizmete, hizmet topolojisi adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="67a76-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="67a76-115">Alternatif olarak, ServiceUnit nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67a76-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="67a76-116">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerServiceUnit cmdlet 'ini kullanarak hizmet birimine değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67a76-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="67a76-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67a76-117">EXAMPLES</span></span>

### <span data-ttu-id="67a76-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67a76-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="67a76-119">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="67a76-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="67a76-120">Örnek 2: kaynak tanımlayıcısını kullanarak bir hizmet birimi alın.</span><span class="sxs-lookup"><span data-stu-id="67a76-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="67a76-121">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="67a76-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="67a76-122">Örnek 3: hizmet birimi nesnesini kullanarak bir hizmet birimi alın.</span><span class="sxs-lookup"><span data-stu-id="67a76-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="67a76-123">Bu komut, adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini alır.</span><span class="sxs-lookup"><span data-stu-id="67a76-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="67a76-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67a76-124">PARAMETERS</span></span>

### <span data-ttu-id="67a76-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a76-125">-DefaultProfile</span></span>
<span data-ttu-id="67a76-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67a76-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a76-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="67a76-127">-Name</span></span>
<span data-ttu-id="67a76-128">Hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="67a76-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a76-129">-ResourceGroupName</span></span>
<span data-ttu-id="67a76-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="67a76-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a76-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="67a76-131">-ResourceId</span></span>
<span data-ttu-id="67a76-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="67a76-132">The resource identifier.</span></span>

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

### <span data-ttu-id="67a76-133">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="67a76-133">-Service</span></span>
<span data-ttu-id="67a76-134">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67a76-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="67a76-135">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="67a76-135">-ServiceName</span></span>
<span data-ttu-id="67a76-136">Hizmet biriminin parçası olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="67a76-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a76-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="67a76-137">-ServiceResourceId</span></span>
<span data-ttu-id="67a76-138">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="67a76-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="67a76-139">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="67a76-139">-ServiceTopology</span></span>
<span data-ttu-id="67a76-140">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67a76-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="67a76-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="67a76-141">-ServiceTopologyName</span></span>
<span data-ttu-id="67a76-142">Hizmet biriminin parçası olan hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="67a76-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="67a76-143">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="67a76-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="67a76-144">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="67a76-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="67a76-145">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="67a76-145">-ServiceUnit</span></span>
<span data-ttu-id="67a76-146">Hizmet birimi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67a76-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="67a76-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a76-147">CommonParameters</span></span>
<span data-ttu-id="67a76-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67a76-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a76-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a76-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a76-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67a76-150">INPUTS</span></span>

### <span data-ttu-id="67a76-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67a76-151">None</span></span>

## <span data-ttu-id="67a76-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67a76-152">OUTPUTS</span></span>

### <span data-ttu-id="67a76-153">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="67a76-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="67a76-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67a76-154">NOTES</span></span>

## <span data-ttu-id="67a76-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67a76-155">RELATED LINKS</span></span>

[<span data-ttu-id="67a76-156">Yeni-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="67a76-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="67a76-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="67a76-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="67a76-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="67a76-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)