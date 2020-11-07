---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916755"
---
# <span data-ttu-id="af7f9-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="af7f9-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="af7f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="af7f9-103">Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="af7f9-103">Create a PSBackend object</span></span>

## <span data-ttu-id="af7f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af7f9-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af7f9-105">DESCRIPTION</span></span>
<span data-ttu-id="af7f9-106">Ön kapı oluşturmak için Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="af7f9-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="af7f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af7f9-107">EXAMPLES</span></span>

### <span data-ttu-id="af7f9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af7f9-108">Example 1</span></span>
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

<span data-ttu-id="af7f9-109">Ön kapı oluşturmak için Psarka uç nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="af7f9-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="af7f9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af7f9-110">PARAMETERS</span></span>

### <span data-ttu-id="af7f9-111">-Adres</span><span class="sxs-lookup"><span data-stu-id="af7f9-111">-Address</span></span>
<span data-ttu-id="af7f9-112">Arka ucun konumu (IP adresi veya FQDN)</span><span class="sxs-lookup"><span data-stu-id="af7f9-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="af7f9-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="af7f9-113">-BackendHostHeader</span></span>
<span data-ttu-id="af7f9-114">Arka uca gönderilen ana bilgisayar üst bilgisi olarak kullanılacak değer.</span><span class="sxs-lookup"><span data-stu-id="af7f9-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="af7f9-115">Varsayılan değer, arka uç adresidir.</span><span class="sxs-lookup"><span data-stu-id="af7f9-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="af7f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7f9-116">-DefaultProfile</span></span>
<span data-ttu-id="af7f9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af7f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af7f9-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="af7f9-118">-EnabledState</span></span>
<span data-ttu-id="af7f9-119">Bu arka ucun kullanımını etkinleştirip etkinleştirmeyeceğinizi.</span><span class="sxs-lookup"><span data-stu-id="af7f9-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="af7f9-120">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="af7f9-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="af7f9-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="af7f9-121">-HttpPort</span></span>
<span data-ttu-id="af7f9-122">HTTP TCP bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="af7f9-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="af7f9-123">1 ile 65535 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af7f9-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="af7f9-124">Varsayılan değer 80 ' dır.</span><span class="sxs-lookup"><span data-stu-id="af7f9-124">Default value is 80.</span></span>

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

### <span data-ttu-id="af7f9-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="af7f9-125">-HttpsPort</span></span>
<span data-ttu-id="af7f9-126">HTTPS TCP bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="af7f9-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="af7f9-127">1 ile 65535 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af7f9-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="af7f9-128">Varsayılan değer 443</span><span class="sxs-lookup"><span data-stu-id="af7f9-128">Default value is 443</span></span>

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

### <span data-ttu-id="af7f9-129">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="af7f9-129">-Priority</span></span>
<span data-ttu-id="af7f9-130">Yük Dengelemesi için kullanılacak öncelik.</span><span class="sxs-lookup"><span data-stu-id="af7f9-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="af7f9-131">1 ile 5 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af7f9-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="af7f9-132">Varsayılan değer 1 ' dir</span><span class="sxs-lookup"><span data-stu-id="af7f9-132">Default value is 1</span></span>

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

### <span data-ttu-id="af7f9-133">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="af7f9-133">-Weight</span></span>
<span data-ttu-id="af7f9-134">Bu uç noktanın yük dengelemesi amaçları için ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="af7f9-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="af7f9-135">1 ile 1000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af7f9-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="af7f9-136">Varsayılan değer 50</span><span class="sxs-lookup"><span data-stu-id="af7f9-136">Default value is 50</span></span>

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

### <span data-ttu-id="af7f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7f9-137">CommonParameters</span></span>
<span data-ttu-id="af7f9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af7f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7f9-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af7f9-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7f9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af7f9-140">INPUTS</span></span>

### <span data-ttu-id="af7f9-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af7f9-141">None</span></span>

## <span data-ttu-id="af7f9-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af7f9-142">OUTPUTS</span></span>

### <span data-ttu-id="af7f9-143">Microsoft. Azure. Commands. Frontkapısı. modeller. Psarka uç</span><span class="sxs-lookup"><span data-stu-id="af7f9-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="af7f9-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af7f9-144">NOTES</span></span>

## <span data-ttu-id="af7f9-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af7f9-145">RELATED LINKS</span></span>

[<span data-ttu-id="af7f9-146">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="af7f9-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
