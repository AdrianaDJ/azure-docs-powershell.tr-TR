---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936846"
---
# <span data-ttu-id="018ff-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="018ff-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="018ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018ff-102">SYNOPSIS</span></span>
<span data-ttu-id="018ff-103">Sanal makinede yedekleme uzantısı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="018ff-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="018ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="018ff-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="018ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="018ff-105">DESCRIPTION</span></span>

## <span data-ttu-id="018ff-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="018ff-106">EXAMPLES</span></span>

### <span data-ttu-id="018ff-107">2</span><span class="sxs-lookup"><span data-stu-id="018ff-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="018ff-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="018ff-108">PARAMETERS</span></span>

### <span data-ttu-id="018ff-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018ff-109">-DefaultProfile</span></span>
<span data-ttu-id="018ff-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="018ff-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="018ff-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="018ff-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="018ff-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018ff-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="018ff-113">Etiketli</span><span class="sxs-lookup"><span data-stu-id="018ff-113">-Tag</span></span>
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

### <span data-ttu-id="018ff-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="018ff-114">-VMName</span></span>
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

### <span data-ttu-id="018ff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018ff-115">CommonParameters</span></span>
<span data-ttu-id="018ff-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="018ff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018ff-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018ff-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018ff-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="018ff-118">INPUTS</span></span>

### <span data-ttu-id="018ff-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="018ff-119">None</span></span>
<span data-ttu-id="018ff-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="018ff-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="018ff-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="018ff-121">OUTPUTS</span></span>

### <span data-ttu-id="018ff-122">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="018ff-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="018ff-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="018ff-123">NOTES</span></span>

## <span data-ttu-id="018ff-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="018ff-124">RELATED LINKS</span></span>

