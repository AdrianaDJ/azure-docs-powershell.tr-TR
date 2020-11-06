---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587539"
---
# <span data-ttu-id="1f90b-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="1f90b-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="1f90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f90b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f90b-103">Uygulama ağ geçidi uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f90b-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f90b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f90b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f90b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f90b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f90b-106">Get-AzureRmApplicationGatewayBackendHealth cmdlet 'i uygulama ağ geçidi uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f90b-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="1f90b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f90b-107">EXAMPLES</span></span>

### <span data-ttu-id="1f90b-108">--------------------------Örnek 1: genişletilmiş kaynaklar olmadan arka uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f90b-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="1f90b-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidinin arka uç durumunu alır ve $BackendHealth değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f90b-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="1f90b-110">--------------------------Örnek 1: genişletilmiş kaynaklarla arka uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f90b-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="1f90b-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidinin arka uç durumunu (genişletilmiş kaynaklarla birlikte) alır ve $BackendHealth değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1f90b-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="1f90b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f90b-112">PARAMETERS</span></span>

### <span data-ttu-id="1f90b-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f90b-113">-AsJob</span></span>
<span data-ttu-id="1f90b-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1f90b-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f90b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f90b-115">-DefaultProfile</span></span>
<span data-ttu-id="1f90b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f90b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f90b-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1f90b-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f90b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f90b-118">-Name</span></span>
<span data-ttu-id="1f90b-119">Bu cmdlet 'in aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f90b-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f90b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f90b-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f90b-121">Uygulama ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f90b-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f90b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f90b-122">CommonParameters</span></span>
<span data-ttu-id="1f90b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f90b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f90b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f90b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f90b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f90b-125">INPUTS</span></span>

### <span data-ttu-id="1f90b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1f90b-126">System.String</span></span>

## <span data-ttu-id="1f90b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f90b-127">OUTPUTS</span></span>

### <span data-ttu-id="1f90b-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="1f90b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="1f90b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f90b-129">NOTES</span></span>
<span data-ttu-id="1f90b-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="1f90b-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1f90b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f90b-131">RELATED LINKS</span></span>

[<span data-ttu-id="1f90b-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f90b-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

