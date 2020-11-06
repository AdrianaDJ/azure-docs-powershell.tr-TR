---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589446"
---
# <span data-ttu-id="7562a-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7562a-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7562a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7562a-102">SYNOPSIS</span></span>
<span data-ttu-id="7562a-103">Uygulama ağ geçidinden güvenilir kök sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7562a-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7562a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7562a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7562a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7562a-105">DESCRIPTION</span></span>
<span data-ttu-id="7562a-106">**Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet 'i, varolan bir uygulama ağ geçidinden güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7562a-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="7562a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7562a-107">EXAMPLES</span></span>

### <span data-ttu-id="7562a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7562a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7562a-109">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7562a-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="7562a-110">İkinci komut, $gw depolanan uygulama ağ geçidinden myRootCA adlı güvenilen kök sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7562a-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="7562a-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7562a-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7562a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7562a-112">PARAMETERS</span></span>

### <span data-ttu-id="7562a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7562a-113">-ApplicationGateway</span></span>
<span data-ttu-id="7562a-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7562a-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7562a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7562a-115">-DefaultProfile</span></span>
<span data-ttu-id="7562a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7562a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7562a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7562a-117">-Name</span></span>
<span data-ttu-id="7562a-118">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="7562a-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7562a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7562a-119">-Confirm</span></span>
<span data-ttu-id="7562a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7562a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7562a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7562a-121">-WhatIf</span></span>
<span data-ttu-id="7562a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7562a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7562a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7562a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7562a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7562a-124">CommonParameters</span></span>
<span data-ttu-id="7562a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7562a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7562a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7562a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7562a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7562a-127">INPUTS</span></span>

### <span data-ttu-id="7562a-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7562a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7562a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7562a-129">OUTPUTS</span></span>

### <span data-ttu-id="7562a-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7562a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7562a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7562a-131">NOTES</span></span>

## <span data-ttu-id="7562a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7562a-132">RELATED LINKS</span></span>
