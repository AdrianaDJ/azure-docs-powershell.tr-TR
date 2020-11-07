---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 94a62f9f65be3f859b088d9e0e1d2561d097e7cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917308"
---
# <span data-ttu-id="f621f-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="f621f-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="f621f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f621f-102">SYNOPSIS</span></span>
<span data-ttu-id="f621f-103">Bir sanal makineden yedeklemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f621f-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="f621f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f621f-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f621f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f621f-105">DESCRIPTION</span></span>

## <span data-ttu-id="f621f-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f621f-106">EXAMPLES</span></span>

### <span data-ttu-id="f621f-107">2</span><span class="sxs-lookup"><span data-stu-id="f621f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f621f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f621f-108">PARAMETERS</span></span>

### <span data-ttu-id="f621f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f621f-109">-DefaultProfile</span></span>
<span data-ttu-id="f621f-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f621f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f621f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f621f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f621f-112">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f621f-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f621f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="f621f-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f621f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f621f-114">CommonParameters</span></span>
<span data-ttu-id="f621f-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f621f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f621f-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f621f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f621f-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f621f-117">INPUTS</span></span>

### <span data-ttu-id="f621f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="f621f-118">System.String</span></span>

## <span data-ttu-id="f621f-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f621f-119">OUTPUTS</span></span>

### <span data-ttu-id="f621f-120">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f621f-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f621f-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f621f-121">NOTES</span></span>

## <span data-ttu-id="f621f-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f621f-122">RELATED LINKS</span></span>
