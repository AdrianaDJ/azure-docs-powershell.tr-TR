---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939750"
---
# <span data-ttu-id="ea17d-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="ea17d-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="ea17d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea17d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea17d-103">Bir sanal makineden yedeklemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea17d-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea17d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea17d-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea17d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea17d-105">DESCRIPTION</span></span>

## <span data-ttu-id="ea17d-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea17d-106">EXAMPLES</span></span>

### <span data-ttu-id="ea17d-107">2</span><span class="sxs-lookup"><span data-stu-id="ea17d-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ea17d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea17d-108">PARAMETERS</span></span>

### <span data-ttu-id="ea17d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea17d-109">-DefaultProfile</span></span>
<span data-ttu-id="ea17d-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea17d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea17d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea17d-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ea17d-112">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ea17d-112">-Tag</span></span>
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

### <span data-ttu-id="ea17d-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="ea17d-113">-VMName</span></span>
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

### <span data-ttu-id="ea17d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea17d-114">CommonParameters</span></span>
<span data-ttu-id="ea17d-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea17d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea17d-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea17d-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea17d-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea17d-117">INPUTS</span></span>

### <span data-ttu-id="ea17d-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ea17d-118">None</span></span>
<span data-ttu-id="ea17d-119">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ea17d-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea17d-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea17d-120">OUTPUTS</span></span>

### <span data-ttu-id="ea17d-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea17d-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea17d-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea17d-122">NOTES</span></span>

## <span data-ttu-id="ea17d-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea17d-123">RELATED LINKS</span></span>

