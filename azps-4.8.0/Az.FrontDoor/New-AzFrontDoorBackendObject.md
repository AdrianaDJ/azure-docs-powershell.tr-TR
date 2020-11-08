---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273579"
---
# <span data-ttu-id="2a915-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="2a915-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="2a915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a915-102">SYNOPSIS</span></span>
<span data-ttu-id="2a915-103">Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a915-103">Create a PSBackend object</span></span>

## <span data-ttu-id="2a915-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a915-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a915-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a915-105">DESCRIPTION</span></span>
<span data-ttu-id="2a915-106">Ön kapı oluşturmak için Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a915-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="2a915-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a915-107">EXAMPLES</span></span>

### <span data-ttu-id="2a915-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a915-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="2a915-109">Ön kapı oluşturmak için Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a915-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="2a915-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a915-110">PARAMETERS</span></span>

### <span data-ttu-id="2a915-111">-Adres</span><span class="sxs-lookup"><span data-stu-id="2a915-111">-Address</span></span>
<span data-ttu-id="2a915-112">Arka ucun konumu (IP adresi veya FQDN)</span><span class="sxs-lookup"><span data-stu-id="2a915-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="2a915-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="2a915-113">-BackendHostHeader</span></span>
<span data-ttu-id="2a915-114">Arka uca gönderilen ana bilgisayar üst bilgisi olarak kullanılacak değer.</span><span class="sxs-lookup"><span data-stu-id="2a915-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="2a915-115">Varsayılan değer, arka uç adresidir.</span><span class="sxs-lookup"><span data-stu-id="2a915-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a915-116">-DefaultProfile</span></span>
<span data-ttu-id="2a915-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a915-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a915-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="2a915-118">-EnabledState</span></span>
<span data-ttu-id="2a915-119">Bu arka ucun kullanımını etkinleştirip etkinleştirmeyeceğinizi.</span><span class="sxs-lookup"><span data-stu-id="2a915-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="2a915-120">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="2a915-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="2a915-121">-HttpPort</span></span>
<span data-ttu-id="2a915-122">HTTP TCP bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="2a915-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="2a915-123">1 ile 65535 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a915-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="2a915-124">Varsayılan değer 80 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2a915-124">Default value is 80.</span></span>

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

### <span data-ttu-id="2a915-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="2a915-125">-HttpsPort</span></span>
<span data-ttu-id="2a915-126">HTTPS TCP bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="2a915-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="2a915-127">1 ile 65535 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a915-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="2a915-128">Varsayılan değer 443</span><span class="sxs-lookup"><span data-stu-id="2a915-128">Default value is 443</span></span>

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

### <span data-ttu-id="2a915-129">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="2a915-129">-Priority</span></span>
<span data-ttu-id="2a915-130">Yük Dengelemesi için kullanılacak öncelik.</span><span class="sxs-lookup"><span data-stu-id="2a915-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="2a915-131">1 ile 5 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a915-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="2a915-132">Varsayılan değer 1 ' dir</span><span class="sxs-lookup"><span data-stu-id="2a915-132">Default value is 1</span></span>

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

### <span data-ttu-id="2a915-133">-Privatelinkalıas</span><span class="sxs-lookup"><span data-stu-id="2a915-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="2a915-134">Özel bağlantı kaynağının diğer adı.</span><span class="sxs-lookup"><span data-stu-id="2a915-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="2a915-135">Bu isteğe bağlı alan doldurulurken, bu uç ucun ' özel ' olduğunu gösterir</span><span class="sxs-lookup"><span data-stu-id="2a915-135">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="2a915-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="2a915-137">Özel bağlantısına bağlanmak için onay isteğine dahil edilecek özel bir ileti</span><span class="sxs-lookup"><span data-stu-id="2a915-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="2a915-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="2a915-139">Özel bağlantı kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="2a915-139">The Location of Private Link resource.</span></span> <span data-ttu-id="2a915-140">Privatelinkresourceıd ayarlandığında konum gereklidir</span><span class="sxs-lookup"><span data-stu-id="2a915-140">Location is required when PrivateLinkResourceId is set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-141">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="2a915-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="2a915-142">Özel bağlantının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2a915-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="2a915-143">Bu isteğe bağlı alan doldurulurken, bu uç ucun ' özel ' olduğunu gösterir</span><span class="sxs-lookup"><span data-stu-id="2a915-143">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a915-144">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="2a915-144">-Weight</span></span>
<span data-ttu-id="2a915-145">Bu uç noktanın yük dengelemesi amaçları için ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="2a915-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="2a915-146">1 ile 1000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a915-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="2a915-147">Varsayılan değer 50</span><span class="sxs-lookup"><span data-stu-id="2a915-147">Default value is 50</span></span>

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

### <span data-ttu-id="2a915-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a915-148">CommonParameters</span></span>
<span data-ttu-id="2a915-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a915-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a915-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a915-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a915-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a915-151">INPUTS</span></span>

### <span data-ttu-id="2a915-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a915-152">None</span></span>

## <span data-ttu-id="2a915-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a915-153">OUTPUTS</span></span>

### <span data-ttu-id="2a915-154">Microsoft. Azure. Commands. Frontkapısı. modeller. Psarka uç</span><span class="sxs-lookup"><span data-stu-id="2a915-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="2a915-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a915-155">NOTES</span></span>

## <span data-ttu-id="2a915-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a915-156">RELATED LINKS</span></span>

[<span data-ttu-id="2a915-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="2a915-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
