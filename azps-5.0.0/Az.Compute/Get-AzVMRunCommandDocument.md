---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279925"
---
# <span data-ttu-id="0cf15-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0cf15-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="0cf15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf15-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf15-103">Bir komut belgesi edinin.</span><span class="sxs-lookup"><span data-stu-id="0cf15-103">Get a run command document.</span></span>

## <span data-ttu-id="0cf15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cf15-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cf15-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf15-106">Bir komut belgesi edinin.</span><span class="sxs-lookup"><span data-stu-id="0cf15-106">Get a run command document.</span></span>

## <span data-ttu-id="0cf15-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cf15-107">EXAMPLES</span></span>

### <span data-ttu-id="0cf15-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0cf15-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="0cf15-109">' Westus ' içindeki ' RunPowerShellScript ' için belirli bir çalıştırma komut belgesini alır.</span><span class="sxs-lookup"><span data-stu-id="0cf15-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="0cf15-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0cf15-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="0cf15-111">' Westus ' içindeki kullanılabilir tüm Run komutlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0cf15-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="0cf15-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cf15-112">PARAMETERS</span></span>

### <span data-ttu-id="0cf15-113">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="0cf15-113">-CommandId</span></span>
<span data-ttu-id="0cf15-114">Komut KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0cf15-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf15-115">-DefaultProfile</span></span>
<span data-ttu-id="0cf15-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0cf15-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf15-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0cf15-117">-Location</span></span>
<span data-ttu-id="0cf15-118">Çalıştırılan komutların sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="0cf15-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="0cf15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf15-119">CommonParameters</span></span>
<span data-ttu-id="0cf15-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cf15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf15-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0cf15-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf15-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cf15-122">INPUTS</span></span>

### <span data-ttu-id="0cf15-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf15-123">System.String</span></span>

## <span data-ttu-id="0cf15-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cf15-124">OUTPUTS</span></span>

### <span data-ttu-id="0cf15-125">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0cf15-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="0cf15-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cf15-126">NOTES</span></span>

## <span data-ttu-id="0cf15-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cf15-127">RELATED LINKS</span></span>
