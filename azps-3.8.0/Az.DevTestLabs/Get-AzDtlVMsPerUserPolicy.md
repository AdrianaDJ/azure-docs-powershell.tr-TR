---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097867"
---
# <span data-ttu-id="80bfb-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="80bfb-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="80bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="80bfb-103">DevTest laboratuvarlarında bir laboratuarın Kullanıcı başına sanal makine ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="80bfb-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="80bfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80bfb-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80bfb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="80bfb-106">**Get-AzDtlVMsPerUserPolicy** cmdlet 'i, bir laboratuvarın Kullanıcı başına sanal makinelerini alır ve Kullanıcı başına izin verilen en fazla sanal makine sayısını ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="80bfb-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="80bfb-107">Cmdlet, ilkenin etkin veya devre dışı durumunu ve ilkede ayarladığınız Kullanıcı başına izin verilen en fazla sanal makine sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="80bfb-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="80bfb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80bfb-108">EXAMPLES</span></span>

## <span data-ttu-id="80bfb-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80bfb-109">PARAMETERS</span></span>

### <span data-ttu-id="80bfb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bfb-110">-DefaultProfile</span></span>
<span data-ttu-id="80bfb-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="80bfb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80bfb-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="80bfb-112">-LabName</span></span>
<span data-ttu-id="80bfb-113">Bu cmdlet 'in Kullanıcı başına sanal makineyi aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80bfb-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="80bfb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bfb-114">-ResourceGroupName</span></span>
<span data-ttu-id="80bfb-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80bfb-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="80bfb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bfb-116">CommonParameters</span></span>
<span data-ttu-id="80bfb-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80bfb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bfb-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80bfb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bfb-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80bfb-119">INPUTS</span></span>

### <span data-ttu-id="80bfb-120">System. String</span><span class="sxs-lookup"><span data-stu-id="80bfb-120">System.String</span></span>

## <span data-ttu-id="80bfb-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80bfb-121">OUTPUTS</span></span>

### <span data-ttu-id="80bfb-122">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="80bfb-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="80bfb-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80bfb-123">NOTES</span></span>

## <span data-ttu-id="80bfb-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80bfb-124">RELATED LINKS</span></span>

[<span data-ttu-id="80bfb-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="80bfb-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


