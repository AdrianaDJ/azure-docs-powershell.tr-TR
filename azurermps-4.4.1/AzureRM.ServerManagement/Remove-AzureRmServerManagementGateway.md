---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590634"
---
# <span data-ttu-id="4e627-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4e627-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="4e627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e627-102">SYNOPSIS</span></span>
<span data-ttu-id="4e627-103">Sunucu yönetimi ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e627-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e627-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e627-104">SYNTAX</span></span>

### <span data-ttu-id="4e627-105">ByName</span><span class="sxs-lookup"><span data-stu-id="4e627-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e627-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="4e627-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e627-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e627-107">DESCRIPTION</span></span>
<span data-ttu-id="4e627-108">**Remove-AzureRmServerManagementGateway** cmdlet 'ı bir Azure Server yönetim ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e627-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="4e627-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e627-109">EXAMPLES</span></span>

## <span data-ttu-id="4e627-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e627-110">PARAMETERS</span></span>

### <span data-ttu-id="4e627-111">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="4e627-111">-Gateway</span></span>
<span data-ttu-id="4e627-112">Bu cmdlet 'in kaldırdığı ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e627-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="4e627-113">Bu parametre, *Resourcegroupname* ve *GatewayName* parametreleri yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4e627-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e627-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="4e627-114">-GatewayName</span></span>
<span data-ttu-id="4e627-115">Bu cmdlet 'in kaldırdığı ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e627-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e627-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e627-116">-ResourceGroupName</span></span>
<span data-ttu-id="4e627-117">Ağ geçidinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e627-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e627-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e627-118">-DefaultProfile</span></span>
<span data-ttu-id="4e627-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e627-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e627-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e627-120">CommonParameters</span></span>
<span data-ttu-id="4e627-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e627-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e627-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e627-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e627-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e627-123">INPUTS</span></span>

### <span data-ttu-id="4e627-124">Geçidi</span><span class="sxs-lookup"><span data-stu-id="4e627-124">Gateway</span></span>
<span data-ttu-id="4e627-125">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4e627-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="4e627-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e627-126">OUTPUTS</span></span>

## <span data-ttu-id="4e627-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e627-127">NOTES</span></span>
* <span data-ttu-id="4e627-128">Bu cmdlet 'i kullanmadan önce ağ geçidinde tüm düğümlerin kaldırılması gerekir; Aksi takdirde bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="4e627-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="4e627-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e627-129">RELATED LINKS</span></span>

[<span data-ttu-id="4e627-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4e627-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="4e627-131">Yeni-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4e627-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


