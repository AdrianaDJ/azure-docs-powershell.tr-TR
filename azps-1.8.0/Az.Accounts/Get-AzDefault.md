---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 374a43b6b094622808f4704daf7063a4c4c0c153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751276"
---
# <span data-ttu-id="b001d-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="b001d-101">Get-AzDefault</span></span>

## <span data-ttu-id="b001d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b001d-102">SYNOPSIS</span></span>
<span data-ttu-id="b001d-103">Geçerli bağlamda Kullanıcı tarafından belirlenen Varsayılanları alın.</span><span class="sxs-lookup"><span data-stu-id="b001d-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="b001d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b001d-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b001d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b001d-105">DESCRIPTION</span></span>
<span data-ttu-id="b001d-106">Get-AzDefault cmdlet 'i, kullanıcının geçerli bağlamda varsayılan olarak ayarlamış olduğu kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="b001d-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="b001d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b001d-107">EXAMPLES</span></span>

### <span data-ttu-id="b001d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b001d-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="b001d-109">Varsayılanlar ayarlanmışsa, bu komut geçerli varsayılanlara döner veya varsayılan olarak ayarlanmamışsa hiçbir şey döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b001d-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="b001d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b001d-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="b001d-111">Varsayılan küme varsa, bu komut geçerli varsayılan kaynak grubunu döndürür veya varsayılan değer ayarlanmamışsa hiçbir şey döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b001d-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="b001d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b001d-112">PARAMETERS</span></span>

### <span data-ttu-id="b001d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b001d-113">-DefaultProfile</span></span>
<span data-ttu-id="b001d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b001d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b001d-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b001d-115">-ResourceGroup</span></span>
<span data-ttu-id="b001d-116">Varsayılan kaynak grubunu görüntüle</span><span class="sxs-lookup"><span data-stu-id="b001d-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b001d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b001d-117">CommonParameters</span></span>
<span data-ttu-id="b001d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b001d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b001d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b001d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b001d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b001d-120">INPUTS</span></span>

### <span data-ttu-id="b001d-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b001d-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b001d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b001d-122">OUTPUTS</span></span>

### <span data-ttu-id="b001d-123">Microsoft. Azure. Commands. Profile. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b001d-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="b001d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b001d-124">NOTES</span></span>

## <span data-ttu-id="b001d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b001d-125">RELATED LINKS</span></span>