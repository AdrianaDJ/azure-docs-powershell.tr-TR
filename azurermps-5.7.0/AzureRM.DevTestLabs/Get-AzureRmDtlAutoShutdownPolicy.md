---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588932"
---
# <span data-ttu-id="49b4a-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="49b4a-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="49b4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="49b4a-103">DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="49b4a-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49b4a-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="49b4a-106">**Get-AzureRmDtlAutoShutdownPolicy** cmdlet 'i, bir laboratuvarın otomatik kapatma ilkesini alır ve belirli bir zamanda bir laboratuvarda tüm sanal makineleri otomatik olarak kapatmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="49b4a-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="49b4a-107">Cmdlet, ilkenin durumunun etkinleştirilip etkinleştirilmediğini ve günün saatini laboratuvar sanal makinelerini otomatik olarak kapatmak için ayarladığınız saat olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="49b4a-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="49b4a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49b4a-108">EXAMPLES</span></span>

## <span data-ttu-id="49b4a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49b4a-109">PARAMETERS</span></span>

### <span data-ttu-id="49b4a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b4a-110">-DefaultProfile</span></span>
<span data-ttu-id="49b4a-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="49b4a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49b4a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="49b4a-112">-LabName</span></span>
<span data-ttu-id="49b4a-113">Bu cmdlet 'in otomatik kapatma ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49b4a-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="49b4a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b4a-114">-ResourceGroupName</span></span>
<span data-ttu-id="49b4a-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49b4a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="49b4a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b4a-116">CommonParameters</span></span>
<span data-ttu-id="49b4a-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49b4a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b4a-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b4a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b4a-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49b4a-119">INPUTS</span></span>

### <span data-ttu-id="49b4a-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="49b4a-120">None</span></span>
<span data-ttu-id="49b4a-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="49b4a-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49b4a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49b4a-122">OUTPUTS</span></span>

### <span data-ttu-id="49b4a-123">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="49b4a-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="49b4a-124">Bu cmdlet, laboratuarın sanal makinelerinin ne zaman kapatılması gerektiğini belirten zamanlamayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="49b4a-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="49b4a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49b4a-125">NOTES</span></span>

## <span data-ttu-id="49b4a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49b4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="49b4a-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="49b4a-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


