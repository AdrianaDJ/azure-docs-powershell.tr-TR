---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 04b226a623a31c73ddd92c858f9ab610a533886f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589562"
---
# <span data-ttu-id="29d55-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="29d55-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="29d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d55-102">SYNOPSIS</span></span>
<span data-ttu-id="29d55-103">DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="29d55-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29d55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29d55-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29d55-105">DESCRIPTION</span></span>
<span data-ttu-id="29d55-106">**Get-AzureRmDtlAutoShutdownPolicy** cmdlet 'i, bir laboratuvarın otomatik kapatma ilkesini alır ve belirli bir zamanda bir laboratuvarda tüm sanal makineleri otomatik olarak kapatmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="29d55-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="29d55-107">Cmdlet, ilkenin durumunun etkinleştirilip etkinleştirilmediğini ve günün saatini laboratuvar sanal makinelerini otomatik olarak kapatmak için ayarladığınız saat olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="29d55-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="29d55-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29d55-108">EXAMPLES</span></span>

## <span data-ttu-id="29d55-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29d55-109">PARAMETERS</span></span>

### <span data-ttu-id="29d55-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d55-110">-DefaultProfile</span></span>
<span data-ttu-id="29d55-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="29d55-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d55-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="29d55-112">-LabName</span></span>
<span data-ttu-id="29d55-113">Bu cmdlet 'in otomatik kapatma ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29d55-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="29d55-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d55-114">-ResourceGroupName</span></span>
<span data-ttu-id="29d55-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29d55-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="29d55-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d55-116">CommonParameters</span></span>
<span data-ttu-id="29d55-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29d55-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d55-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d55-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d55-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29d55-119">INPUTS</span></span>

### <span data-ttu-id="29d55-120">System. String</span><span class="sxs-lookup"><span data-stu-id="29d55-120">System.String</span></span>

## <span data-ttu-id="29d55-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29d55-121">OUTPUTS</span></span>

### <span data-ttu-id="29d55-122">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="29d55-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="29d55-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29d55-123">NOTES</span></span>

## <span data-ttu-id="29d55-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29d55-124">RELATED LINKS</span></span>

[<span data-ttu-id="29d55-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="29d55-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


