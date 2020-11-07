---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: c61739c3bd80c5c5c15c7e10d8a787f45c44ec69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762533"
---
# <span data-ttu-id="1a46f-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="1a46f-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="1a46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a46f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a46f-103">DevTest laboratuvarlarında bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1a46f-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a46f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a46f-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a46f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a46f-105">DESCRIPTION</span></span>
<span data-ttu-id="1a46f-106">**Get-AzureRmDtlAutoStartPolicy** cmdlet 'i, otomatik başlatma için laboratuvar sanal makineleri zamanlayan bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1a46f-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="1a46f-107">Cmdlet, ilkenin etkin veya devre dışı durumunu ve hafta sanal makinelerinin otomatik başlatma için sanal makinelere izin verecek şekilde ayarladığınız haftanın günlerini ve günün saatini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a46f-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="1a46f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a46f-108">EXAMPLES</span></span>

## <span data-ttu-id="1a46f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a46f-109">PARAMETERS</span></span>

### <span data-ttu-id="1a46f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a46f-110">-DefaultProfile</span></span>
<span data-ttu-id="1a46f-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1a46f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a46f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="1a46f-112">-LabName</span></span>
<span data-ttu-id="1a46f-113">Bu cmdlet 'in otomatik başlangıç ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a46f-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a46f-114">-ResourceGroupName</span></span>
<span data-ttu-id="1a46f-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a46f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a46f-116">CommonParameters</span></span>
<span data-ttu-id="1a46f-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a46f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a46f-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a46f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a46f-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a46f-119">INPUTS</span></span>

### <span data-ttu-id="1a46f-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1a46f-120">None</span></span>
<span data-ttu-id="1a46f-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1a46f-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a46f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a46f-122">OUTPUTS</span></span>

### <span data-ttu-id="1a46f-123">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="1a46f-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="1a46f-124">Bu cmdlet, laboratuarın sanal makinelerinin başlatılması gereken zamanını belirten zamanlamayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a46f-124">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="1a46f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a46f-125">NOTES</span></span>

## <span data-ttu-id="1a46f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a46f-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a46f-127">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="1a46f-127">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


