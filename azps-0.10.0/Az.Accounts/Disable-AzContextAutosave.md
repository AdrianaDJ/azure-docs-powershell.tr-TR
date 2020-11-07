---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: f268c4171be78265843d5a04291bf430dc4f19b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935280"
---
# <span data-ttu-id="a821d-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a821d-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="a821d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a821d-102">SYNOPSIS</span></span>
<span data-ttu-id="a821d-103">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="a821d-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="a821d-104">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="a821d-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="a821d-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a821d-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a821d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="a821d-106">DESCRIPTION</span></span>
<span data-ttu-id="a821d-107">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="a821d-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="a821d-108">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="a821d-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="a821d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a821d-109">EXAMPLES</span></span>

### <span data-ttu-id="a821d-110">Bağlamı otomatik kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a821d-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="a821d-111">Geçerli Kullanıcı için otomatik kaydetmeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="a821d-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="a821d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a821d-112">PARAMETERS</span></span>

### <span data-ttu-id="a821d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a821d-113">-DefaultProfile</span></span>
<span data-ttu-id="a821d-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a821d-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a821d-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a821d-115">-Scope</span></span>
<span data-ttu-id="a821d-116">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="a821d-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a821d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a821d-117">-Confirm</span></span>
<span data-ttu-id="a821d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a821d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a821d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a821d-119">-WhatIf</span></span>
<span data-ttu-id="a821d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a821d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a821d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a821d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a821d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a821d-122">CommonParameters</span></span>
<span data-ttu-id="a821d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a821d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a821d-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a821d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a821d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a821d-125">INPUTS</span></span>

### <span data-ttu-id="a821d-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a821d-126">None</span></span>

## <span data-ttu-id="a821d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a821d-127">OUTPUTS</span></span>

### <span data-ttu-id="a821d-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="a821d-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="a821d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a821d-129">NOTES</span></span>

## <span data-ttu-id="a821d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a821d-130">RELATED LINKS</span></span>
