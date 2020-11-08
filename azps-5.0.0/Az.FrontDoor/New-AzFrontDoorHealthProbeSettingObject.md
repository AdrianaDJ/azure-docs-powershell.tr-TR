---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277415"
---
# <span data-ttu-id="67133-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="67133-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="67133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67133-102">SYNOPSIS</span></span>
<span data-ttu-id="67133-103">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="67133-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="67133-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67133-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67133-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67133-105">DESCRIPTION</span></span>
<span data-ttu-id="67133-106">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="67133-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="67133-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67133-107">EXAMPLES</span></span>

### <span data-ttu-id="67133-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67133-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="67133-109">Not: HealthProbeMethod ayarı büyük/küçük harfe duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="67133-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="67133-110">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="67133-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="67133-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67133-111">PARAMETERS</span></span>

### <span data-ttu-id="67133-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67133-112">-DefaultProfile</span></span>
<span data-ttu-id="67133-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67133-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67133-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="67133-114">-EnabledState</span></span>
<span data-ttu-id="67133-115">BackendPools altında tanımlanan backends 'ye karşı sistem durumu sonlarının yapılabilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="67133-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="67133-116">Sistem durumu sonları, yalnızca tek etkinleştirilmiş uç havuzda tek etkinleştirilmiş bir arka uç olduğunda devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="67133-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="67133-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="67133-117">-HealthProbeMethod</span></span>
<span data-ttu-id="67133-118">BackendPools altında tanımlanan backends 'yi araştırırsa hangi HTTP yönteminin kullanılacağını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="67133-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="67133-119">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="67133-119">-IntervalInSeconds</span></span>
<span data-ttu-id="67133-120">Sağlık sondaları arasındaki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="67133-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="67133-121">Varsayılan değer 30</span><span class="sxs-lookup"><span data-stu-id="67133-121">Default value is 30</span></span>

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

### <span data-ttu-id="67133-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="67133-122">-Name</span></span>
<span data-ttu-id="67133-123">Durum araştırma ayarı adı.</span><span class="sxs-lookup"><span data-stu-id="67133-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="67133-124">-Yol</span><span class="sxs-lookup"><span data-stu-id="67133-124">-Path</span></span>
<span data-ttu-id="67133-125">Sistem durumu araştırması için kullanılacak yol.</span><span class="sxs-lookup"><span data-stu-id="67133-125">The path to use for the health probe.</span></span>
<span data-ttu-id="67133-126">Varsayılan/</span><span class="sxs-lookup"><span data-stu-id="67133-126">Default is /</span></span>

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

### <span data-ttu-id="67133-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="67133-127">-Protocol</span></span>
<span data-ttu-id="67133-128">Bu yoklama için kullanılacak protokol düzeni varsayılan değer HTTP</span><span class="sxs-lookup"><span data-stu-id="67133-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67133-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67133-129">CommonParameters</span></span>
<span data-ttu-id="67133-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67133-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67133-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67133-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67133-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67133-132">INPUTS</span></span>

### <span data-ttu-id="67133-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67133-133">None</span></span>
## <span data-ttu-id="67133-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67133-134">OUTPUTS</span></span>

### <span data-ttu-id="67133-135">Microsoft. Azure. Commands. Frontkapısı. modeller. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="67133-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="67133-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67133-136">NOTES</span></span>

## <span data-ttu-id="67133-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67133-137">RELATED LINKS</span></span>

<span data-ttu-id="67133-138">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="67133-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
