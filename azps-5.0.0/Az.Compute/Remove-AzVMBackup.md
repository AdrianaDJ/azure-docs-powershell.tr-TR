---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322234"
---
# <span data-ttu-id="0a420-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="0a420-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="0a420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a420-102">SYNOPSIS</span></span>
<span data-ttu-id="0a420-103">Bir sanal makineden yedeklemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a420-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="0a420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a420-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a420-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a420-105">DESCRIPTION</span></span>

## <span data-ttu-id="0a420-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a420-106">EXAMPLES</span></span>

### <span data-ttu-id="0a420-107">2</span><span class="sxs-lookup"><span data-stu-id="0a420-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0a420-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a420-108">PARAMETERS</span></span>

### <span data-ttu-id="0a420-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a420-109">-DefaultProfile</span></span>
<span data-ttu-id="0a420-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a420-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a420-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a420-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0a420-112">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0a420-112">-Tag</span></span>
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

### <span data-ttu-id="0a420-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a420-113">-VMName</span></span>
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

### <span data-ttu-id="0a420-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a420-114">CommonParameters</span></span>
<span data-ttu-id="0a420-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a420-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a420-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a420-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a420-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a420-117">INPUTS</span></span>

### <span data-ttu-id="0a420-118">System. String</span><span class="sxs-lookup"><span data-stu-id="0a420-118">System.String</span></span>

## <span data-ttu-id="0a420-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a420-119">OUTPUTS</span></span>

### <span data-ttu-id="0a420-120">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0a420-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0a420-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a420-121">NOTES</span></span>

## <span data-ttu-id="0a420-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a420-122">RELATED LINKS</span></span>
