---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937008"
---
# <span data-ttu-id="a1cdd-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="a1cdd-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="a1cdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cdd-103">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-103">Get run command document.</span></span>

## <span data-ttu-id="a1cdd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1cdd-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1cdd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="a1cdd-106">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-106">Get run command document.</span></span>

## <span data-ttu-id="a1cdd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="a1cdd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1cdd-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="a1cdd-109">' Westus ' içindeki ' RunPowerShellScript ' için belirli bir çalıştırma komut belgesini alır.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="a1cdd-110">Get-AzVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="a1cdd-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="a1cdd-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a1cdd-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="a1cdd-112">' Westus ' içindeki kullanılabilir tüm Run komutlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="a1cdd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1cdd-113">PARAMETERS</span></span>

### <span data-ttu-id="a1cdd-114">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="a1cdd-114">-CommandId</span></span>
<span data-ttu-id="a1cdd-115">Komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-115">The command id.</span></span>

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

### <span data-ttu-id="a1cdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cdd-116">-DefaultProfile</span></span>
<span data-ttu-id="a1cdd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1cdd-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1cdd-118">-Location</span></span>
<span data-ttu-id="a1cdd-119">Çalıştırılan komutların sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="a1cdd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cdd-120">CommonParameters</span></span>
<span data-ttu-id="a1cdd-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cdd-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1cdd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cdd-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1cdd-123">INPUTS</span></span>

### <span data-ttu-id="a1cdd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a1cdd-124">System.String</span></span>

## <span data-ttu-id="a1cdd-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1cdd-125">OUTPUTS</span></span>

### <span data-ttu-id="a1cdd-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="a1cdd-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="a1cdd-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1cdd-127">NOTES</span></span>

## <span data-ttu-id="a1cdd-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1cdd-128">RELATED LINKS</span></span>

