---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4717fa187a8bd8234cd786ff5c6ad6d1678696b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763742"
---
# <span data-ttu-id="b86d7-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b86d7-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="b86d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b86d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b86d7-103">DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b86d7-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b86d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b86d7-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b86d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b86d7-105">DESCRIPTION</span></span>
<span data-ttu-id="b86d7-106">**Get-AzureRmDtlAutoShutdownPolicy** cmdlet 'i, bir laboratuvarın otomatik kapatma ilkesini alır ve belirli bir zamanda bir laboratuvarda tüm sanal makineleri otomatik olarak kapatmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b86d7-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="b86d7-107">Cmdlet, ilkenin durumunun etkinleştirilip etkinleştirilmediğini ve günün saatini laboratuvar sanal makinelerini otomatik olarak kapatmak için ayarladığınız saat olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b86d7-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="b86d7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b86d7-108">EXAMPLES</span></span>

## <span data-ttu-id="b86d7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b86d7-109">PARAMETERS</span></span>

### <span data-ttu-id="b86d7-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="b86d7-110">-LabName</span></span>
<span data-ttu-id="b86d7-111">Bu cmdlet 'in otomatik kapatma ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b86d7-111">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86d7-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b86d7-112">-ResourceGroupName</span></span>
<span data-ttu-id="b86d7-113">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b86d7-113">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86d7-114">-DefaultProfile</span></span>
<span data-ttu-id="b86d7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b86d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b86d7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86d7-116">CommonParameters</span></span>
<span data-ttu-id="b86d7-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b86d7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86d7-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86d7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86d7-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b86d7-119">INPUTS</span></span>

## <span data-ttu-id="b86d7-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b86d7-120">OUTPUTS</span></span>

### <span data-ttu-id="b86d7-121">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b86d7-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="b86d7-122">Bu cmdlet, laboratuarın sanal makinelerinin ne zaman kapatılması gerektiğini belirten zamanlamayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="b86d7-122">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="b86d7-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b86d7-123">NOTES</span></span>

## <span data-ttu-id="b86d7-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b86d7-124">RELATED LINKS</span></span>

[<span data-ttu-id="b86d7-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b86d7-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


