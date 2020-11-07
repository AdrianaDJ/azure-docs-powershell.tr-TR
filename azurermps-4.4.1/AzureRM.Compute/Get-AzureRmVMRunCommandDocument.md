---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765195"
---
# <span data-ttu-id="6b3b3-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6b3b3-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="6b3b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3b3-103">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b3b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b3b3-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b3b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b3b3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b3b3-106">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-106">Get run command document.</span></span>

## <span data-ttu-id="6b3b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b3b3-107">EXAMPLES</span></span>

### <span data-ttu-id="6b3b3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6b3b3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="6b3b3-109">' Westus ' içindeki ' RunPowerShellScript ' için belirli bir çalıştırma komut belgesini alır.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="6b3b3-110">Get-AzureRmVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="6b3b3-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="6b3b3-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6b3b3-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="6b3b3-112">' Westus ' içindeki kullanılabilir tüm Run komutlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="6b3b3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b3b3-113">PARAMETERS</span></span>

### <span data-ttu-id="6b3b3-114">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="6b3b3-114">-CommandId</span></span>
<span data-ttu-id="6b3b3-115">Komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3b3-116">-DefaultProfile</span></span>
<span data-ttu-id="6b3b3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3b3-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="6b3b3-118">-Location</span></span>
<span data-ttu-id="6b3b3-119">Çalıştırılan komutların sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="6b3b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3b3-120">CommonParameters</span></span>
<span data-ttu-id="6b3b3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b3b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3b3-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b3b3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3b3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b3b3-123">INPUTS</span></span>

### <span data-ttu-id="6b3b3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6b3b3-124">System.String</span></span>

## <span data-ttu-id="6b3b3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b3b3-125">OUTPUTS</span></span>

### <span data-ttu-id="6b3b3-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6b3b3-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="6b3b3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b3b3-127">NOTES</span></span>

## <span data-ttu-id="6b3b3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b3b3-128">RELATED LINKS</span></span>

