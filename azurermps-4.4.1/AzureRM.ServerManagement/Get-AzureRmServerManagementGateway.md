---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762691"
---
# <span data-ttu-id="c2d28-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c2d28-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="c2d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d28-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d28-103">Bir veya daha fazla sunucu yönetimi ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2d28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2d28-104">SYNTAX</span></span>

### <span data-ttu-id="c2d28-105">NoParams (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2d28-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d28-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c2d28-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d28-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="c2d28-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d28-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="c2d28-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2d28-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2d28-109">DESCRIPTION</span></span>
<span data-ttu-id="c2d28-110">**Get-AzureRmServerManagementGateway** cmdlet 'i bir veya daha fazla Azure Server Management Gateway alır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="c2d28-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2d28-111">EXAMPLES</span></span>

### <span data-ttu-id="c2d28-112">Örnek 1: abonelikteki tüm ağ geçitlerini alma</span><span class="sxs-lookup"><span data-stu-id="c2d28-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="c2d28-113">Bu komut, abonelikteki tüm sunucu yönetimi ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="c2d28-114">Örnek 2: kaynak grubundaki ağ geçitlerini alma</span><span class="sxs-lookup"><span data-stu-id="c2d28-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="c2d28-115">Bu komut, Group001 adlı kaynak grubuna ait olan tüm sunucu yönetimi ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="c2d28-116">Örnek 3: bir ağ geçidinin tüm yüklü örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="c2d28-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="c2d28-117">Bu komut, Group002 adındaki kaynak grubuna ait olan Gateway01 adındaki bir sunucu yönetimi ağ geçidinin tüm örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="c2d28-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2d28-118">PARAMETERS</span></span>

### <span data-ttu-id="c2d28-119">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="c2d28-119">-Gateway</span></span>
<span data-ttu-id="c2d28-120">Bu cmdlet 'in aldığı ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2d28-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="c2d28-121">Cmdlet, eylemi gerçekleştirmek için belirtilen ağ geçidi aracılığıyla *Resourcegroupname* ve *GatewayName* parametrelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2d28-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="c2d28-122">Bu parametre belirtildiğinde, bu cmdlet ağ geçidi için ayrıntılı durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="c2d28-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d28-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="c2d28-123">-GatewayName</span></span>
<span data-ttu-id="c2d28-124">Bu cmdlet 'in kapısı aldığı sunucu yönetimi ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2d28-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="c2d28-125">*GatewayName* parametresini belirttiğinizde, bu cmdlet ağ geçidinde ayrıntılı durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="c2d28-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d28-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d28-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2d28-127">Bu cmdlet ağ geçitleri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2d28-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d28-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d28-128">-DefaultProfile</span></span>
<span data-ttu-id="c2d28-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2d28-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2d28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d28-130">CommonParameters</span></span>
<span data-ttu-id="c2d28-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2d28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d28-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2d28-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d28-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2d28-133">INPUTS</span></span>

### <span data-ttu-id="c2d28-134">Geçidi</span><span class="sxs-lookup"><span data-stu-id="c2d28-134">Gateway</span></span>
<span data-ttu-id="c2d28-135">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c2d28-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="c2d28-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2d28-136">OUTPUTS</span></span>

### <span data-ttu-id="c2d28-137">Microsoft. Azure. Commands. ServerManagement. model. geçit</span><span class="sxs-lookup"><span data-stu-id="c2d28-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="c2d28-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2d28-138">NOTES</span></span>
* <span data-ttu-id="c2d28-139">Bu cmdlet parametre olmadan kullanıyorsanız, abonelikle ilişkilendirilmiş tüm ağ geçitleri döner.</span><span class="sxs-lookup"><span data-stu-id="c2d28-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="c2d28-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2d28-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2d28-141">Yeni-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c2d28-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="c2d28-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c2d28-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


