---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936921"
---
# <span data-ttu-id="27c88-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="27c88-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="27c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c88-102">SYNOPSIS</span></span>
<span data-ttu-id="27c88-103">Bir sanal makineden yedeklemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="27c88-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="27c88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27c88-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27c88-105">DESCRIPTION</span></span>

## <span data-ttu-id="27c88-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27c88-106">EXAMPLES</span></span>

### <span data-ttu-id="27c88-107">2</span><span class="sxs-lookup"><span data-stu-id="27c88-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="27c88-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27c88-108">PARAMETERS</span></span>

### <span data-ttu-id="27c88-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c88-109">-DefaultProfile</span></span>
<span data-ttu-id="27c88-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27c88-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27c88-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c88-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="27c88-112">Etiketli</span><span class="sxs-lookup"><span data-stu-id="27c88-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c88-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="27c88-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c88-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c88-114">CommonParameters</span></span>
<span data-ttu-id="27c88-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27c88-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c88-116">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c88-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c88-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27c88-117">INPUTS</span></span>

### <span data-ttu-id="27c88-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="27c88-118">None</span></span>
<span data-ttu-id="27c88-119">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="27c88-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27c88-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27c88-120">OUTPUTS</span></span>

### <span data-ttu-id="27c88-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="27c88-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="27c88-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27c88-122">NOTES</span></span>

## <span data-ttu-id="27c88-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27c88-123">RELATED LINKS</span></span>

