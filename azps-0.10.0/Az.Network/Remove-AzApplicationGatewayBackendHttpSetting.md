---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 168223e9e442b7aa37da11f3a1e0a092c3cb3efc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935331"
---
# <span data-ttu-id="0d5a4-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0d5a4-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="0d5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5a4-103">Uygulama ağ geçidinden arka uç HTTP ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="0d5a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d5a4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d5a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5a4-106">Remove-AzApplicationGatewayBackendHttpSetting cmdlet 'i bir Azure uygulama ağ geçidinden arka uç köprü metni Aktarma Protokolü (HTTP) ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="0d5a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d5a4-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5a4-108">Örnek 1: uygulama ağ geçidinden geri açılan HTTP ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0d5a4-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="0d5a4-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0d5a4-110">İkinci komut, BackEndSetting02 adlı geri dönüş HTTP ayarını $AppGw depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0d5a4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d5a4-111">PARAMETERS</span></span>

### <span data-ttu-id="0d5a4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5a4-112">-ApplicationGateway</span></span>
<span data-ttu-id="0d5a4-113">Bu cmdlet 'in arka uç HTTP ayarlarını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5a4-114">-DefaultProfile</span></span>
<span data-ttu-id="0d5a4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5a4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d5a4-116">-Name</span></span>
<span data-ttu-id="0d5a4-117">Bu cmdlet 'in kaldırdığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5a4-118">CommonParameters</span></span>
<span data-ttu-id="0d5a4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5a4-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5a4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5a4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d5a4-121">INPUTS</span></span>

### <span data-ttu-id="0d5a4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0d5a4-122">System.String</span></span>

## <span data-ttu-id="0d5a4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d5a4-123">OUTPUTS</span></span>

### <span data-ttu-id="0d5a4-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5a4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d5a4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d5a4-125">NOTES</span></span>

## <span data-ttu-id="0d5a4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d5a4-126">RELATED LINKS</span></span>

[<span data-ttu-id="0d5a4-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0d5a4-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0d5a4-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0d5a4-128">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0d5a4-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0d5a4-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0d5a4-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0d5a4-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

