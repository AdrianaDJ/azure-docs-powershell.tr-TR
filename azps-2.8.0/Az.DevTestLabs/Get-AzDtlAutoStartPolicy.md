---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 449206713291499c344975e490c3b0d89ab1d88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752092"
---
# <span data-ttu-id="5672b-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="5672b-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="5672b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5672b-102">SYNOPSIS</span></span>
<span data-ttu-id="5672b-103">DevTest laboratuvarlarında bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="5672b-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5672b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5672b-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5672b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5672b-105">DESCRIPTION</span></span>
<span data-ttu-id="5672b-106">**Get-AzDtlAutoStartPolicy** cmdlet 'i, otomatik başlatma için laboratuvar sanal makineleri zamanlayan bir laboratuvarın otomatik başlatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="5672b-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="5672b-107">Cmdlet, ilkenin etkin veya devre dışı durumunu ve hafta sanal makinelerinin otomatik başlatma için sanal makinelere izin verecek şekilde ayarladığınız haftanın günlerini ve günün saatini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5672b-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="5672b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5672b-108">EXAMPLES</span></span>

## <span data-ttu-id="5672b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5672b-109">PARAMETERS</span></span>

### <span data-ttu-id="5672b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5672b-110">-DefaultProfile</span></span>
<span data-ttu-id="5672b-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5672b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5672b-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="5672b-112">-LabName</span></span>
<span data-ttu-id="5672b-113">Bu cmdlet 'in otomatik başlangıç ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5672b-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="5672b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5672b-114">-ResourceGroupName</span></span>
<span data-ttu-id="5672b-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5672b-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5672b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5672b-116">CommonParameters</span></span>
<span data-ttu-id="5672b-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5672b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5672b-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5672b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5672b-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5672b-119">INPUTS</span></span>

### <span data-ttu-id="5672b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5672b-120">System.String</span></span>

## <span data-ttu-id="5672b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5672b-121">OUTPUTS</span></span>

### <span data-ttu-id="5672b-122">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="5672b-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="5672b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5672b-123">NOTES</span></span>

## <span data-ttu-id="5672b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5672b-124">RELATED LINKS</span></span>

[<span data-ttu-id="5672b-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="5672b-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


