---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6c0e557078bde5cbec7b1f7dd96f1fa2c71408a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935266"
---
# <span data-ttu-id="b6507-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b6507-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="b6507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6507-102">SYNOPSIS</span></span>
<span data-ttu-id="b6507-103">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="b6507-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="b6507-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6507-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6507-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6507-105">DESCRIPTION</span></span>
<span data-ttu-id="b6507-106">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="b6507-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="b6507-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6507-107">EXAMPLES</span></span>

### <span data-ttu-id="b6507-108">Geçerli Kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b6507-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="b6507-109">Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma.</span><span class="sxs-lookup"><span data-stu-id="b6507-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="b6507-110">Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.</span><span class="sxs-lookup"><span data-stu-id="b6507-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="b6507-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6507-111">PARAMETERS</span></span>

### <span data-ttu-id="b6507-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6507-112">-DefaultProfile</span></span>
<span data-ttu-id="b6507-113">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6507-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6507-114">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="b6507-114">-Scope</span></span>
<span data-ttu-id="b6507-115">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="b6507-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b6507-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6507-116">-Confirm</span></span>
<span data-ttu-id="b6507-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6507-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6507-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6507-118">-WhatIf</span></span>
<span data-ttu-id="b6507-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6507-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6507-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6507-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6507-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6507-121">CommonParameters</span></span>
<span data-ttu-id="b6507-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6507-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6507-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6507-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6507-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6507-124">INPUTS</span></span>

### <span data-ttu-id="b6507-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6507-125">None</span></span>

## <span data-ttu-id="b6507-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6507-126">OUTPUTS</span></span>

### <span data-ttu-id="b6507-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b6507-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b6507-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6507-128">NOTES</span></span>

## <span data-ttu-id="b6507-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6507-129">RELATED LINKS</span></span>
