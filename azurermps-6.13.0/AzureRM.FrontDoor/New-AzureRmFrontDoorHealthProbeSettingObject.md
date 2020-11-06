---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590289"
---
# <span data-ttu-id="d862a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="d862a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="d862a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d862a-102">SYNOPSIS</span></span>
<span data-ttu-id="d862a-103">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d862a-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d862a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d862a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d862a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d862a-105">DESCRIPTION</span></span>
<span data-ttu-id="d862a-106">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d862a-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d862a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d862a-107">EXAMPLES</span></span>

### <span data-ttu-id="d862a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d862a-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="d862a-109">Ön kapı oluşturmak için PSHealthProbeSetting nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d862a-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d862a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d862a-110">PARAMETERS</span></span>

### <span data-ttu-id="d862a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d862a-111">-DefaultProfile</span></span>
<span data-ttu-id="d862a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d862a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d862a-113">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="d862a-113">-IntervalInSeconds</span></span>
<span data-ttu-id="d862a-114">Sağlık sondaları arasındaki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="d862a-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="d862a-115">Varsayılan değer 30</span><span class="sxs-lookup"><span data-stu-id="d862a-115">Default value is 30</span></span>

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

### <span data-ttu-id="d862a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d862a-116">-Name</span></span>
<span data-ttu-id="d862a-117">durum araştırma ayarı adı.</span><span class="sxs-lookup"><span data-stu-id="d862a-117">health probe setting name.</span></span>

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

### <span data-ttu-id="d862a-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="d862a-118">-Path</span></span>
<span data-ttu-id="d862a-119">Sistem durumu araştırması için kullanılacak yol.</span><span class="sxs-lookup"><span data-stu-id="d862a-119">The path to use for the health probe.</span></span>
<span data-ttu-id="d862a-120">Varsayılan/</span><span class="sxs-lookup"><span data-stu-id="d862a-120">Default is /</span></span>

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

### <span data-ttu-id="d862a-121">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d862a-121">-Protocol</span></span>
<span data-ttu-id="d862a-122">Bu yoklama için kullanılacak protokol düzeni varsayılan değer HTTP</span><span class="sxs-lookup"><span data-stu-id="d862a-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="d862a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d862a-123">CommonParameters</span></span>
<span data-ttu-id="d862a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d862a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d862a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d862a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d862a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d862a-126">INPUTS</span></span>

### <span data-ttu-id="d862a-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d862a-127">None</span></span>

## <span data-ttu-id="d862a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d862a-128">OUTPUTS</span></span>

### <span data-ttu-id="d862a-129">Microsoft. Azure. Commands. Frontkapısı. modeller. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d862a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="d862a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d862a-130">NOTES</span></span>

## <span data-ttu-id="d862a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d862a-131">RELATED LINKS</span></span>

<span data-ttu-id="d862a-132">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d862a-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
