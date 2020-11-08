---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 2ad9574cbd50c4100dbda7b35a64e557b195898a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097841"
---
# <span data-ttu-id="2f5fe-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="2f5fe-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="2f5fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5fe-103">DevTest laboratuvarlarında bir laboratuvarın otomatik kapatma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="2f5fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f5fe-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f5fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5fe-106">**Get-AzDtlAutoShutdownPolicy** cmdlet 'i, bir laboratuvarın otomatik kapatma ilkesini alır ve bu, belirli bir zamanda laboratuarda tüm sanal makineleri otomatik olarak kapatmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="2f5fe-107">Cmdlet, ilkenin durumunun etkinleştirilip etkinleştirilmediğini ve günün saatini laboratuvar sanal makinelerini otomatik olarak kapatmak için ayarladığınız saat olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="2f5fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f5fe-108">EXAMPLES</span></span>

## <span data-ttu-id="2f5fe-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f5fe-109">PARAMETERS</span></span>

### <span data-ttu-id="2f5fe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5fe-110">-DefaultProfile</span></span>
<span data-ttu-id="2f5fe-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2f5fe-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f5fe-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="2f5fe-112">-LabName</span></span>
<span data-ttu-id="2f5fe-113">Bu cmdlet 'in otomatik kapatma ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="2f5fe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5fe-114">-ResourceGroupName</span></span>
<span data-ttu-id="2f5fe-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2f5fe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5fe-116">CommonParameters</span></span>
<span data-ttu-id="2f5fe-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f5fe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5fe-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f5fe-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5fe-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f5fe-119">INPUTS</span></span>

### <span data-ttu-id="2f5fe-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2f5fe-120">System.String</span></span>

## <span data-ttu-id="2f5fe-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f5fe-121">OUTPUTS</span></span>

### <span data-ttu-id="2f5fe-122">Microsoft. Azure. Commands. DevTestLabs. model. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="2f5fe-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="2f5fe-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f5fe-123">NOTES</span></span>

## <span data-ttu-id="2f5fe-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f5fe-124">RELATED LINKS</span></span>

[<span data-ttu-id="2f5fe-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="2f5fe-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


