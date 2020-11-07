---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938790"
---
# <span data-ttu-id="9b2c2-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9b2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2c2-103">Uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b2c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b2c2-104">SYNTAX</span></span>

### <span data-ttu-id="9b2c2-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9b2c2-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b2c2-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2c2-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="9b2c2-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b2c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b2c2-108">DESCRIPTION</span></span>
<span data-ttu-id="9b2c2-109">**New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'i bir uygulama ağ geçidi için Yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="9b2c2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b2c2-110">EXAMPLES</span></span>

### <span data-ttu-id="9b2c2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b2c2-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="9b2c2-112">Bu komut, Redirect01 adlı bir yönlendirme yapılandırması oluşturur ve sonucu $RedirectConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="9b2c2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="9b2c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2c2-114">-DefaultProfile</span></span>
<span data-ttu-id="9b2c2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2c2-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="9b2c2-116">-IncludePath</span></span>
<span data-ttu-id="9b2c2-117">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-117">Include path in the redirected url.</span></span>
<span data-ttu-id="9b2c2-118">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-119">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="9b2c2-119">-IncludeQueryString</span></span>
<span data-ttu-id="9b2c2-120">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="9b2c2-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b2c2-122">-Name</span></span>
<span data-ttu-id="9b2c2-123">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="9b2c2-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="9b2c2-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="9b2c2-124">-RedirectType</span></span>
<span data-ttu-id="9b2c2-125">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="9b2c2-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="9b2c2-126">-TargetListener</span></span>
<span data-ttu-id="9b2c2-127">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="9b2c2-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-128">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="9b2c2-128">-TargetListenerID</span></span>
<span data-ttu-id="9b2c2-129">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="9b2c2-129">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="9b2c2-130">-TargetUrl</span></span>
<span data-ttu-id="9b2c2-131">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="9b2c2-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2c2-132">CommonParameters</span></span>
<span data-ttu-id="9b2c2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2c2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2c2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b2c2-135">INPUTS</span></span>

### <span data-ttu-id="9b2c2-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9b2c2-136">None</span></span>

## <span data-ttu-id="9b2c2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b2c2-137">OUTPUTS</span></span>

### <span data-ttu-id="9b2c2-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9b2c2-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b2c2-139">NOTES</span></span>

## <span data-ttu-id="9b2c2-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b2c2-140">RELATED LINKS</span></span>

