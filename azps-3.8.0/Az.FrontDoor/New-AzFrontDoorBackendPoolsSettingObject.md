---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937476"
---
# <span data-ttu-id="b65d3-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="b65d3-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="b65d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b65d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b65d3-103">Ön kapı oluşturmak için PSBackendPoolsSetting nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b65d3-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="b65d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b65d3-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b65d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b65d3-106">**New-AzFrontDoorBackendpoolsSettingObject** cmdlet 'ı ön kapı oluşturmak için yeni bir PSBackendPoolsSettings nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b65d3-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="b65d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b65d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b65d3-108">Örnek 1: Varsayılanları kullanarak BackendPoolsSettings nesnesini oluşturma</span><span class="sxs-lookup"><span data-stu-id="b65d3-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="b65d3-109">Örnek 2: kullanıcının belirttiği değerleri içeren BackendPoolsSettings nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b65d3-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="b65d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b65d3-110">PARAMETERS</span></span>

### <span data-ttu-id="b65d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65d3-111">-DefaultProfile</span></span>
<span data-ttu-id="b65d3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b65d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65d3-113">-Enforcecercertificate Atenamecheck</span><span class="sxs-lookup"><span data-stu-id="b65d3-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="b65d3-114">HTTPS isteklerinin tüm arka uç havuzlarına sertifika adı denetimini zorunlu tutma.</span><span class="sxs-lookup"><span data-stu-id="b65d3-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="b65d3-115">HTTPS olmayan isteklerde hiçbir etkiye gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="b65d3-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="b65d3-116">-Sendrecvtimeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="b65d3-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="b65d3-117">İsteğin arka uca iletilmesi sırasında zaman aşımı gönderme ve alma.</span><span class="sxs-lookup"><span data-stu-id="b65d3-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="b65d3-118">Zaman aşımına ulaşıldığında, istek başarısız olur ve geri döner.</span><span class="sxs-lookup"><span data-stu-id="b65d3-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="b65d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65d3-119">CommonParameters</span></span>
<span data-ttu-id="b65d3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b65d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65d3-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b65d3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65d3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b65d3-122">INPUTS</span></span>

### <span data-ttu-id="b65d3-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b65d3-123">None</span></span>

## <span data-ttu-id="b65d3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b65d3-124">OUTPUTS</span></span>

### <span data-ttu-id="b65d3-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="b65d3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="b65d3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b65d3-126">NOTES</span></span>

## <span data-ttu-id="b65d3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b65d3-127">RELATED LINKS</span></span>