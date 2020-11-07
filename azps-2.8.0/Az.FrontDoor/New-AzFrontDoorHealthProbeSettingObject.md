---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751901"
---
# <span data-ttu-id="11aef-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="11aef-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="11aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11aef-102">SYNOPSIS</span></span>
<span data-ttu-id="11aef-103">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="11aef-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="11aef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11aef-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11aef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11aef-105">DESCRIPTION</span></span>
<span data-ttu-id="11aef-106">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="11aef-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="11aef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11aef-107">EXAMPLES</span></span>

### <span data-ttu-id="11aef-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11aef-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="11aef-109">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="11aef-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="11aef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11aef-110">PARAMETERS</span></span>

### <span data-ttu-id="11aef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11aef-111">-DefaultProfile</span></span>
<span data-ttu-id="11aef-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11aef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11aef-113">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="11aef-113">-IntervalInSeconds</span></span>
<span data-ttu-id="11aef-114">Sağlık sondaları arasındaki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="11aef-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="11aef-115">Varsayılan değer 30</span><span class="sxs-lookup"><span data-stu-id="11aef-115">Default value is 30</span></span>

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

### <span data-ttu-id="11aef-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="11aef-116">-Name</span></span>
<span data-ttu-id="11aef-117">durum araştırma ayarı adı.</span><span class="sxs-lookup"><span data-stu-id="11aef-117">health probe setting name.</span></span>

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

### <span data-ttu-id="11aef-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="11aef-118">-Path</span></span>
<span data-ttu-id="11aef-119">Sistem durumu araştırması için kullanılacak yol.</span><span class="sxs-lookup"><span data-stu-id="11aef-119">The path to use for the health probe.</span></span>
<span data-ttu-id="11aef-120">Varsayılan/</span><span class="sxs-lookup"><span data-stu-id="11aef-120">Default is /</span></span>

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

### <span data-ttu-id="11aef-121">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="11aef-121">-Protocol</span></span>
<span data-ttu-id="11aef-122">Bu yoklama için kullanılacak protokol düzeni varsayılan değer HTTP</span><span class="sxs-lookup"><span data-stu-id="11aef-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="11aef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11aef-123">CommonParameters</span></span>
<span data-ttu-id="11aef-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11aef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11aef-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="11aef-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11aef-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11aef-126">INPUTS</span></span>

### <span data-ttu-id="11aef-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="11aef-127">None</span></span>

## <span data-ttu-id="11aef-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11aef-128">OUTPUTS</span></span>

### <span data-ttu-id="11aef-129">Microsoft. Azure. Commands. Frontkapısı. modeller. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="11aef-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="11aef-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11aef-130">NOTES</span></span>

## <span data-ttu-id="11aef-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11aef-131">RELATED LINKS</span></span>

<span data-ttu-id="11aef-132">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="11aef-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>