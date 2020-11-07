---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 50d0345fea26d233147ad8373ab3daae785d6715
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763740"
---
# <span data-ttu-id="3b680-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="3b680-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="3b680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b680-102">SYNOPSIS</span></span>
<span data-ttu-id="3b680-103">DevTest laboratuvarlarında bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b680-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b680-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b680-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b680-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b680-105">DESCRIPTION</span></span>
<span data-ttu-id="3b680-106">**Get-AzureRmDtlAutoStartPolicy** cmdlet 'i, otomatik başlatma için laboratuvar sanal makineleri zamanlayan bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b680-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="3b680-107">Cmdlet, ilkenin etkin veya devre dışı durumunu ve hafta sanal makinelerinin otomatik başlatma için sanal makinelere izin verecek şekilde ayarladığınız haftanın günlerini ve günün saatini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b680-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="3b680-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b680-108">EXAMPLES</span></span>

## <span data-ttu-id="3b680-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b680-109">PARAMETERS</span></span>

### <span data-ttu-id="3b680-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="3b680-110">-LabName</span></span>
<span data-ttu-id="3b680-111">Bu cmdlet 'in otomatik başlangıç ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b680-111">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="3b680-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b680-112">-ResourceGroupName</span></span>
<span data-ttu-id="3b680-113">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b680-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="3b680-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b680-114">-DefaultProfile</span></span>
<span data-ttu-id="3b680-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b680-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b680-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b680-116">CommonParameters</span></span>
<span data-ttu-id="3b680-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b680-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b680-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b680-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b680-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b680-119">INPUTS</span></span>

## <span data-ttu-id="3b680-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b680-120">OUTPUTS</span></span>

### <span data-ttu-id="3b680-121">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="3b680-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="3b680-122">Bu cmdlet, laboratuarın sanal makinelerinin başlatılması gereken zamanını belirten zamanlamayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b680-122">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="3b680-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b680-123">NOTES</span></span>

## <span data-ttu-id="3b680-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b680-124">RELATED LINKS</span></span>

[<span data-ttu-id="3b680-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="3b680-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)

