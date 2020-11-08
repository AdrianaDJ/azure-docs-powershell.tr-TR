---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097842"
---
# <span data-ttu-id="d28fb-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d28fb-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="d28fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d28fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d28fb-103">DevTest laboratuvarlarında bir laboratuvarın izin verilen sanal makine boyutları ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d28fb-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d28fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d28fb-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d28fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d28fb-105">DESCRIPTION</span></span>
<span data-ttu-id="d28fb-106">**Get-AzDtlAllowedVMSizesPolicy** cmdlet 'i, laboratuvarda izin verilen sanal makine boyutlarının listesini belirtmenize olanak sağlayan izin verilen sanal makine boyutları ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d28fb-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="d28fb-107">Cmdlet ilkenin etkin veya devre dışı durumunu ve belirtilen ilkede ayarlamış olduğunuz tüm izin verilen sanal makine boyutlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d28fb-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="d28fb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d28fb-108">EXAMPLES</span></span>

## <span data-ttu-id="d28fb-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d28fb-109">PARAMETERS</span></span>

### <span data-ttu-id="d28fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28fb-110">-DefaultProfile</span></span>
<span data-ttu-id="d28fb-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d28fb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d28fb-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d28fb-112">-LabName</span></span>
<span data-ttu-id="d28fb-113">Bu cmdlet 'in sanal makine boyutu ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d28fb-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="d28fb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28fb-114">-ResourceGroupName</span></span>
<span data-ttu-id="d28fb-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d28fb-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d28fb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28fb-116">CommonParameters</span></span>
<span data-ttu-id="d28fb-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d28fb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28fb-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d28fb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28fb-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d28fb-119">INPUTS</span></span>

### <span data-ttu-id="d28fb-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d28fb-120">System.String</span></span>

## <span data-ttu-id="d28fb-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d28fb-121">OUTPUTS</span></span>

### <span data-ttu-id="d28fb-122">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d28fb-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d28fb-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d28fb-123">NOTES</span></span>

## <span data-ttu-id="d28fb-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d28fb-124">RELATED LINKS</span></span>

[<span data-ttu-id="d28fb-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d28fb-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


