---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108916"
---
# <span data-ttu-id="a1f36-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a1f36-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="a1f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f36-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f36-103">Güvenlik duvarı ilkesi için ilke ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="a1f36-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="a1f36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1f36-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1f36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1f36-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f36-106">**Yeni-AzApplicationGatewayFirewallPolicySetting** , güvenlik duvarı ilkesi için ilke ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1f36-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="a1f36-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1f36-107">EXAMPLES</span></span>

### <span data-ttu-id="a1f36-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1f36-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="a1f36-109">Bu komut, MaxRequestBodySizeInKb olarak mod, $enabledMode olarak mod, RequestBodyCheck, FileUploadLimitInMb 'yi $fileUploadLimitInMb ve as $ $maxRequestBodySizeInKb $enabledState ile bir ilke ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1f36-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="a1f36-110">Yeni policySettings $condition depolanır.</span><span class="sxs-lookup"><span data-stu-id="a1f36-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="a1f36-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1f36-111">PARAMETERS</span></span>

### <span data-ttu-id="a1f36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f36-112">-DefaultProfile</span></span>
<span data-ttu-id="a1f36-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1f36-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f36-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="a1f36-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="a1f36-115">Güvenlik Duvarı ilkesinin ilke ayarlarında requestBodyCheck Diables.</span><span class="sxs-lookup"><span data-stu-id="a1f36-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f36-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="a1f36-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="a1f36-117">MB cinsinden en büyük fileUpload boyutu.</span><span class="sxs-lookup"><span data-stu-id="a1f36-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f36-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="a1f36-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="a1f36-119">Güvenlik Duvarı ilkesinin ilke ayarlarında MaxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="a1f36-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f36-120">-Mod</span><span class="sxs-lookup"><span data-stu-id="a1f36-120">-Mode</span></span>
<span data-ttu-id="a1f36-121">Güvenlik Duvarı ilkesinin ilke ayarlarında güvenlik duvarı modu.</span><span class="sxs-lookup"><span data-stu-id="a1f36-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f36-122">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a1f36-122">-State</span></span>
<span data-ttu-id="a1f36-123">Güvenlik Duvarı ilkesinin ilke ayarlarındaki durum değişkeni.</span><span class="sxs-lookup"><span data-stu-id="a1f36-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f36-124">CommonParameters</span></span>
<span data-ttu-id="a1f36-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1f36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f36-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1f36-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f36-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1f36-127">INPUTS</span></span>

### <span data-ttu-id="a1f36-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1f36-128">None</span></span>

## <span data-ttu-id="a1f36-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1f36-129">OUTPUTS</span></span>

### <span data-ttu-id="a1f36-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="a1f36-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="a1f36-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1f36-131">NOTES</span></span>

## <span data-ttu-id="a1f36-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1f36-132">RELATED LINKS</span></span>
