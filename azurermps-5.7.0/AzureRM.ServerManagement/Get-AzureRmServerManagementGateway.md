---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573281"
---
# <span data-ttu-id="03224-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="03224-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="03224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03224-102">SYNOPSIS</span></span>
<span data-ttu-id="03224-103">Bir veya daha fazla sunucu yönetimi ağ geçidi alır.</span><span class="sxs-lookup"><span data-stu-id="03224-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03224-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03224-104">SYNTAX</span></span>

### <span data-ttu-id="03224-105">NoParams (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03224-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03224-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="03224-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03224-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="03224-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03224-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="03224-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03224-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="03224-109">DESCRIPTION</span></span>
<span data-ttu-id="03224-110">**Get-AzureRmServerManagementGateway** cmdlet 'i bir veya daha fazla Azure Server Management Gateway alır.</span><span class="sxs-lookup"><span data-stu-id="03224-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="03224-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03224-111">EXAMPLES</span></span>

### <span data-ttu-id="03224-112">Örnek 1: abonelikteki tüm ağ geçitlerini alma</span><span class="sxs-lookup"><span data-stu-id="03224-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="03224-113">Bu komut, abonelikteki tüm sunucu yönetimi ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="03224-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="03224-114">Örnek 2: kaynak grubundaki ağ geçitlerini alma</span><span class="sxs-lookup"><span data-stu-id="03224-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="03224-115">Bu komut, Group001 adlı kaynak grubuna ait olan tüm sunucu yönetimi ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="03224-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="03224-116">Örnek 3: bir ağ geçidinin tüm yüklü örneklerini alma</span><span class="sxs-lookup"><span data-stu-id="03224-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="03224-117">Bu komut, Group002 adındaki kaynak grubuna ait olan Gateway01 adındaki bir sunucu yönetimi ağ geçidinin tüm örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="03224-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="03224-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03224-118">PARAMETERS</span></span>

### <span data-ttu-id="03224-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03224-119">-DefaultProfile</span></span>
<span data-ttu-id="03224-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03224-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03224-121">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="03224-121">-Gateway</span></span>
<span data-ttu-id="03224-122">Bu cmdlet 'in aldığı ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="03224-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="03224-123">Cmdlet, eylemi gerçekleştirmek için belirtilen ağ geçidi aracılığıyla *Resourcegroupname* ve *GatewayName* parametrelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="03224-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="03224-124">Bu parametre belirtildiğinde, bu cmdlet ağ geçidi için ayrıntılı durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="03224-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03224-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="03224-125">-GatewayName</span></span>
<span data-ttu-id="03224-126">Bu cmdlet 'in kapısı aldığı sunucu yönetimi ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03224-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="03224-127">*GatewayName* parametresini belirttiğinizde, bu cmdlet ağ geçidinde ayrıntılı durumu içerir.</span><span class="sxs-lookup"><span data-stu-id="03224-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03224-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03224-128">-ResourceGroupName</span></span>
<span data-ttu-id="03224-129">Bu cmdlet ağ geçitleri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03224-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03224-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03224-130">CommonParameters</span></span>
<span data-ttu-id="03224-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03224-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03224-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03224-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03224-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03224-133">INPUTS</span></span>

### <span data-ttu-id="03224-134">Geçidi</span><span class="sxs-lookup"><span data-stu-id="03224-134">Gateway</span></span>
<span data-ttu-id="03224-135">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="03224-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="03224-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03224-136">OUTPUTS</span></span>

### <span data-ttu-id="03224-137">Microsoft. Azure. Commands. ServerManagement. model. geçit</span><span class="sxs-lookup"><span data-stu-id="03224-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="03224-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03224-138">NOTES</span></span>
* <span data-ttu-id="03224-139">Bu cmdlet parametre olmadan kullanıyorsanız, abonelikle ilişkilendirilmiş tüm ağ geçitleri döner.</span><span class="sxs-lookup"><span data-stu-id="03224-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="03224-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03224-140">RELATED LINKS</span></span>

[<span data-ttu-id="03224-141">Yeni-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="03224-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="03224-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="03224-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


