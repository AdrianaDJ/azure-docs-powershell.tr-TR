---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 7430402d62d88ea192b94166f48c0657e47cbf15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762238"
---
# <span data-ttu-id="c1d6c-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="c1d6c-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="c1d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d6c-103">Geçerli bağlamda Kullanıcı tarafından belirlenen Varsayılanları alın.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1d6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1d6c-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d6c-106">Get-AzureRmDefault cmdlet 'i, kullanıcının geçerli bağlamda varsayılan olarak ayarlamış olduğu kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="c1d6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d6c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1d6c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="c1d6c-109">Varsayılanlar ayarlanmışsa, bu komut geçerli varsayılanlara döner veya varsayılan olarak ayarlanmamışsa hiçbir şey döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="c1d6c-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c1d6c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="c1d6c-111">Varsayılan küme varsa, bu komut geçerli varsayılan kaynak grubunu döndürür veya varsayılan değer ayarlanmamışsa hiçbir şey döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="c1d6c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1d6c-112">PARAMETERS</span></span>

### <span data-ttu-id="c1d6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d6c-113">-DefaultProfile</span></span>
<span data-ttu-id="c1d6c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d6c-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1d6c-115">-ResourceGroup</span></span>
<span data-ttu-id="c1d6c-116">Varsayılan kaynak grubunu görüntüle</span><span class="sxs-lookup"><span data-stu-id="c1d6c-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="c1d6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d6c-117">CommonParameters</span></span>
<span data-ttu-id="c1d6c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1d6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d6c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d6c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d6c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1d6c-120">INPUTS</span></span>

### <span data-ttu-id="c1d6c-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1d6c-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1d6c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1d6c-122">OUTPUTS</span></span>

### <span data-ttu-id="c1d6c-123">Microsoft. Azure. Commands. Profile. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1d6c-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="c1d6c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1d6c-124">NOTES</span></span>

## <span data-ttu-id="c1d6c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1d6c-125">RELATED LINKS</span></span>
