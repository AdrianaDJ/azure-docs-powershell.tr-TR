---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939566"
---
# <span data-ttu-id="c5398-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="c5398-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="c5398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5398-102">SYNOPSIS</span></span>
<span data-ttu-id="c5398-103">Sanal makinede yedekleme uzantısı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c5398-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5398-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5398-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5398-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5398-105">DESCRIPTION</span></span>

## <span data-ttu-id="c5398-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5398-106">EXAMPLES</span></span>

### <span data-ttu-id="c5398-107">2</span><span class="sxs-lookup"><span data-stu-id="c5398-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c5398-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5398-108">PARAMETERS</span></span>

### <span data-ttu-id="c5398-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5398-109">-DefaultProfile</span></span>
<span data-ttu-id="c5398-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5398-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5398-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5398-111">-Name</span></span>
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

### <span data-ttu-id="c5398-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5398-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c5398-113">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c5398-113">-Tag</span></span>
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

### <span data-ttu-id="c5398-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5398-114">-VMName</span></span>
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

### <span data-ttu-id="c5398-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5398-115">CommonParameters</span></span>
<span data-ttu-id="c5398-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5398-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5398-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5398-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5398-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5398-118">INPUTS</span></span>

### <span data-ttu-id="c5398-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c5398-119">None</span></span>
<span data-ttu-id="c5398-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c5398-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5398-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5398-121">OUTPUTS</span></span>

### <span data-ttu-id="c5398-122">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c5398-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c5398-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5398-123">NOTES</span></span>

## <span data-ttu-id="c5398-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5398-124">RELATED LINKS</span></span>

