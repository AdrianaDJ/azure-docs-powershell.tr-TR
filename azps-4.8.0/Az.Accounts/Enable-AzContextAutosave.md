---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267404"
---
# <span data-ttu-id="07827-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="07827-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="07827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07827-102">SYNOPSIS</span></span>
<span data-ttu-id="07827-103">Azure bağlamları, komutları çalıştırmak için etkin aboneliğinizi ve bir Azure bulutuna bağlanmak için gereken kimlik doğrulama bilgilerini temsil eden PowerShell nesneleridir.</span><span class="sxs-lookup"><span data-stu-id="07827-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="07827-104">Azure bağlamlarıyla, abonelikleri değiştirdiğinizde Azure PowerShell 'in hesabınızı yeniden doğrulaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="07827-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="07827-105">Daha fazla bilgi [için bkz.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="07827-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="07827-106">Bu cmdlet, bir PowerShell işlemini başlattığınızda Azure bağlam bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="07827-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="07827-107">Örneğin, yeni bir pencere açarken.</span><span class="sxs-lookup"><span data-stu-id="07827-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="07827-108">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07827-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07827-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="07827-109">DESCRIPTION</span></span>

<span data-ttu-id="07827-110">Bir PowerShell süreci başlatıldığında Azure bağlam bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="07827-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="07827-111">Bağlam, içeriği etkileyen tüm cmdlet yürütmesinin sonunda kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="07827-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="07827-112">Örneğin, herhangi bir profil cmdlet 'i.</span><span class="sxs-lookup"><span data-stu-id="07827-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="07827-113">Kullanıcı kimlik doğrulamasını kullanıyorsanız, belirteçler çalıştırma sırasında belirteçler güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="07827-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="07827-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07827-114">EXAMPLES</span></span>

### <span data-ttu-id="07827-115">Örnek 1: geçerli kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="07827-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="07827-116">Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma.</span><span class="sxs-lookup"><span data-stu-id="07827-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="07827-117">Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.</span><span class="sxs-lookup"><span data-stu-id="07827-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="07827-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="07827-118">Example 2</span></span>

<span data-ttu-id="07827-119">Bu PowerShell oturumunda, bir PowerShell penceresini açtığınızda Azure kimlik bilgileri, hesap ve abonelik bilgilerine izin verin ve otomatik olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="07827-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="07827-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="07827-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="07827-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07827-121">PARAMETERS</span></span>

### <span data-ttu-id="07827-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07827-122">-DefaultProfile</span></span>

<span data-ttu-id="07827-123">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="07827-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="07827-124">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="07827-124">-Scope</span></span>

<span data-ttu-id="07827-125">Bağlam değişikliklerinin kapsamını belirler.</span><span class="sxs-lookup"><span data-stu-id="07827-125">Determines the scope of context changes.</span></span> <span data-ttu-id="07827-126">Örneğin, değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="07827-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="07827-127">Kapsamla yapılan değişiklikler, `CurrentUser` Kullanıcı tarafından başlatılan tüm PowerShell oturumlarını etkiler.</span><span class="sxs-lookup"><span data-stu-id="07827-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="07827-128">Belirli bir oturumun farklı ayarları olması gerekiyorsa, kapsamı kullanın `Process` .</span><span class="sxs-lookup"><span data-stu-id="07827-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07827-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="07827-129">-Confirm</span></span>

<span data-ttu-id="07827-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07827-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07827-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07827-131">-WhatIf</span></span>

<span data-ttu-id="07827-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07827-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07827-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07827-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="07827-134">Ortak Parametreler</span><span class="sxs-lookup"><span data-stu-id="07827-134">Common Parameters</span></span>

<span data-ttu-id="07827-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07827-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07827-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07827-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07827-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07827-137">INPUTS</span></span>

### <span data-ttu-id="07827-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07827-138">None</span></span>

## <span data-ttu-id="07827-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07827-139">OUTPUTS</span></span>

### <span data-ttu-id="07827-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="07827-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="07827-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07827-141">NOTES</span></span>

## <span data-ttu-id="07827-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07827-142">RELATED LINKS</span></span>
