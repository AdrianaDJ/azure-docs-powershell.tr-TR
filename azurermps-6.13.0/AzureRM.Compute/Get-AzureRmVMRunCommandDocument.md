---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: 070fe50f74db08caab375a97d4d8ff6be3e970ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589581"
---
# <span data-ttu-id="10443-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="10443-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="10443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10443-102">SYNOPSIS</span></span>
<span data-ttu-id="10443-103">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="10443-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10443-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10443-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10443-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10443-105">DESCRIPTION</span></span>
<span data-ttu-id="10443-106">Run komut belgesini alın.</span><span class="sxs-lookup"><span data-stu-id="10443-106">Get run command document.</span></span>

## <span data-ttu-id="10443-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10443-107">EXAMPLES</span></span>

### <span data-ttu-id="10443-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10443-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="10443-109">' Westus ' içindeki ' RunPowerShellScript ' için belirli bir çalıştırma komut belgesini alır.</span><span class="sxs-lookup"><span data-stu-id="10443-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>
<span data-ttu-id="10443-110">Get-AzureRmVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="10443-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="10443-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="10443-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="10443-112">' Westus ' içindeki kullanılabilir tüm Run komutlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="10443-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="10443-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10443-113">PARAMETERS</span></span>

### <span data-ttu-id="10443-114">-Commanmuydunuz</span><span class="sxs-lookup"><span data-stu-id="10443-114">-CommandId</span></span>
<span data-ttu-id="10443-115">Komut kimliği.</span><span class="sxs-lookup"><span data-stu-id="10443-115">The command id.</span></span>

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

### <span data-ttu-id="10443-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10443-116">-DefaultProfile</span></span>
<span data-ttu-id="10443-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10443-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10443-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="10443-118">-Location</span></span>
<span data-ttu-id="10443-119">Çalıştırılan komutların sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="10443-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="10443-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10443-120">CommonParameters</span></span>
<span data-ttu-id="10443-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10443-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10443-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10443-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10443-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10443-123">INPUTS</span></span>

### <span data-ttu-id="10443-124">System. String</span><span class="sxs-lookup"><span data-stu-id="10443-124">System.String</span></span>

## <span data-ttu-id="10443-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10443-125">OUTPUTS</span></span>

### <span data-ttu-id="10443-126">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="10443-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="10443-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10443-127">NOTES</span></span>

## <span data-ttu-id="10443-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10443-128">RELATED LINKS</span></span>
