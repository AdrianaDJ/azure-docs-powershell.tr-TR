---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572441"
---
# <span data-ttu-id="5635a-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5635a-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="5635a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5635a-102">SYNOPSIS</span></span>
<span data-ttu-id="5635a-103">Hizmet topolojisinde hizmet alır.</span><span class="sxs-lookup"><span data-stu-id="5635a-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="5635a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5635a-104">SYNTAX</span></span>

### <span data-ttu-id="5635a-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5635a-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5635a-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5635a-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5635a-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5635a-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5635a-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5635a-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5635a-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="5635a-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5635a-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="5635a-110">DESCRIPTION</span></span>
<span data-ttu-id="5635a-111">**Get-AzureRmDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet alır ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5635a-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="5635a-112">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="5635a-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="5635a-113">Alternatif olarak, servis nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5635a-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="5635a-114">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5635a-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="5635a-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5635a-115">EXAMPLES</span></span>

### <span data-ttu-id="5635a-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5635a-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="5635a-117">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde alır.</span><span class="sxs-lookup"><span data-stu-id="5635a-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5635a-118">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet alma.</span><span class="sxs-lookup"><span data-stu-id="5635a-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="5635a-119">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde alır.</span><span class="sxs-lookup"><span data-stu-id="5635a-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5635a-120">Örnek 3: hizmet nesnesini kullanarak hizmet alma.</span><span class="sxs-lookup"><span data-stu-id="5635a-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="5635a-121">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="5635a-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="5635a-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5635a-122">PARAMETERS</span></span>

### <span data-ttu-id="5635a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5635a-123">-DefaultProfile</span></span>
<span data-ttu-id="5635a-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5635a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5635a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5635a-125">-Name</span></span>
<span data-ttu-id="5635a-126">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="5635a-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5635a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5635a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5635a-128">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5635a-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5635a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5635a-129">-ResourceId</span></span>
<span data-ttu-id="5635a-130">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5635a-130">The resource identifier.</span></span>

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

### <span data-ttu-id="5635a-131">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="5635a-131">-Service</span></span>
<span data-ttu-id="5635a-132">Hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5635a-132">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5635a-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5635a-133">-ServiceTopology</span></span>
<span data-ttu-id="5635a-134">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5635a-134">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5635a-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="5635a-135">-ServiceTopologyName</span></span>
<span data-ttu-id="5635a-136">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="5635a-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="5635a-137">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5635a-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="5635a-138">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="5635a-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5635a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5635a-139">CommonParameters</span></span>
<span data-ttu-id="5635a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5635a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5635a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5635a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5635a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5635a-142">INPUTS</span></span>

### <span data-ttu-id="5635a-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5635a-143">None</span></span>

## <span data-ttu-id="5635a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5635a-144">OUTPUTS</span></span>

### <span data-ttu-id="5635a-145">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="5635a-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="5635a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5635a-146">NOTES</span></span>

## <span data-ttu-id="5635a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5635a-147">RELATED LINKS</span></span>

[<span data-ttu-id="5635a-148">Yeni-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5635a-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="5635a-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5635a-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="5635a-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5635a-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)