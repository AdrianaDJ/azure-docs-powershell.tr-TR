---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: df53acc047ff0c17b3482f214c357f66ce638efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764477"
---
# <span data-ttu-id="73907-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="73907-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="73907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73907-102">SYNOPSIS</span></span>
<span data-ttu-id="73907-103">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="73907-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73907-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73907-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73907-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73907-105">DESCRIPTION</span></span>
<span data-ttu-id="73907-106">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="73907-106">Get run command document.</span></span>

## <span data-ttu-id="73907-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73907-107">EXAMPLES</span></span>

### <span data-ttu-id="73907-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73907-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="73907-109">' Westus ' içindeki ' RunPowerShellScript ' için belirli bir çalıştırma komut belgesini alır.</span><span class="sxs-lookup"><span data-stu-id="73907-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="73907-110">Get-AzureRmVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="73907-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="73907-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="73907-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="73907-112">' Westus ' içindeki kullanılabilir tüm Run komutlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="73907-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="73907-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73907-113">PARAMETERS</span></span>

### <span data-ttu-id="73907-114">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="73907-114">-CommandId</span></span>
<span data-ttu-id="73907-115">Komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="73907-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73907-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73907-116">-DefaultProfile</span></span>
<span data-ttu-id="73907-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73907-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73907-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="73907-118">-Location</span></span>
<span data-ttu-id="73907-119">Çalıştırılan komutların sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="73907-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73907-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73907-120">CommonParameters</span></span>
<span data-ttu-id="73907-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73907-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73907-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73907-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73907-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73907-123">INPUTS</span></span>

### <span data-ttu-id="73907-124">System. String</span><span class="sxs-lookup"><span data-stu-id="73907-124">System.String</span></span>

## <span data-ttu-id="73907-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73907-125">OUTPUTS</span></span>

### <span data-ttu-id="73907-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="73907-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="73907-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73907-127">NOTES</span></span>

## <span data-ttu-id="73907-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73907-128">RELATED LINKS</span></span>
