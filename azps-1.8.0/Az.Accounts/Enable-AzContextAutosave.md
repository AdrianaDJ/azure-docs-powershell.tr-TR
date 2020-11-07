---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: eedd28fe1df7992658dfe9b36ebab58e77eb87c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751284"
---
# <span data-ttu-id="ad614-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="ad614-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="ad614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad614-102">SYNOPSIS</span></span>
<span data-ttu-id="ad614-103">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="ad614-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="ad614-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad614-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad614-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad614-105">DESCRIPTION</span></span>
<span data-ttu-id="ad614-106">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="ad614-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="ad614-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad614-107">EXAMPLES</span></span>

### <span data-ttu-id="ad614-108">Geçerli Kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ad614-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="ad614-109">Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma.</span><span class="sxs-lookup"><span data-stu-id="ad614-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="ad614-110">Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.</span><span class="sxs-lookup"><span data-stu-id="ad614-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="ad614-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad614-111">PARAMETERS</span></span>

### <span data-ttu-id="ad614-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad614-112">-DefaultProfile</span></span>
<span data-ttu-id="ad614-113">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ad614-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad614-114">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ad614-114">-Scope</span></span>
<span data-ttu-id="ad614-115">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="ad614-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ad614-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad614-116">-Confirm</span></span>
<span data-ttu-id="ad614-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad614-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad614-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad614-118">-WhatIf</span></span>
<span data-ttu-id="ad614-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad614-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad614-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad614-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad614-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad614-121">CommonParameters</span></span>
<span data-ttu-id="ad614-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad614-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad614-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad614-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad614-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad614-124">INPUTS</span></span>

### <span data-ttu-id="ad614-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad614-125">None</span></span>

## <span data-ttu-id="ad614-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad614-126">OUTPUTS</span></span>

### <span data-ttu-id="ad614-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ad614-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="ad614-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad614-128">NOTES</span></span>

## <span data-ttu-id="ad614-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad614-129">RELATED LINKS</span></span>
