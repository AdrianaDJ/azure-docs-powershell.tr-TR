---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: a55844251e7d84ef24d62195b96b9bd4c3934317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751285"
---
# <span data-ttu-id="32bf6-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="32bf6-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="32bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="32bf6-103">Bağlı bir Azure hesabının bağlantısını keser ve bu hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32bf6-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="32bf6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32bf6-104">SYNTAX</span></span>

### <span data-ttu-id="32bf6-105">ContextName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32bf6-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bf6-106">Desteklenmeyen</span><span class="sxs-lookup"><span data-stu-id="32bf6-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bf6-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32bf6-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bf6-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="32bf6-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bf6-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="32bf6-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bf6-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="32bf6-110">DESCRIPTION</span></span>
<span data-ttu-id="32bf6-111">Disconnect-AzAccount cmdlet 'i bağlı bir Azure hesabının bağlantısını keser ve bu Firmayla ilişkili tüm kimlik bilgilerini ve bağlamları (abonelik ve kiracı bilgileri) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32bf6-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="32bf6-112">Bu cmdlet 'i çalıştırdıktan sonra Connect-AzAccount kullanarak yeniden oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="32bf6-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="32bf6-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32bf6-113">EXAMPLES</span></span>

### <span data-ttu-id="32bf6-114">Geçerli hesabın oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="32bf6-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="32bf6-115">Geçerli içerikle ilişkili Azure hesabından oturum açar.</span><span class="sxs-lookup"><span data-stu-id="32bf6-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="32bf6-116">Belirli bir içerikle ilişkili hesabın oturumu kapatma</span><span class="sxs-lookup"><span data-stu-id="32bf6-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="32bf6-117">Verilen içerikle ilişkili hesabı (' çalışma ' adlı) günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="32bf6-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="32bf6-118">Bu, ' CurrentUser ' kapsamını kullandığı için tüm kimlik bilgileri ve bağlamlar kalıcı olarak silinecektir.</span><span class="sxs-lookup"><span data-stu-id="32bf6-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="32bf6-119">Belirli bir kullanıcının oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="32bf6-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="32bf6-120">' user1@contoso.org ' Kullanıcıyı-tüm kimlik bilgilerini ve bu kullanıcıyla ilişkili tüm bağlamları günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="32bf6-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="32bf6-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32bf6-121">PARAMETERS</span></span>

### <span data-ttu-id="32bf6-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="32bf6-122">-ApplicationId</span></span>
<span data-ttu-id="32bf6-123">ServicePrincipal ID (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="32bf6-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="32bf6-124">-AzureContext</span></span>
<span data-ttu-id="32bf6-125">Dan</span><span class="sxs-lookup"><span data-stu-id="32bf6-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="32bf6-126">-ContextName</span></span>
<span data-ttu-id="32bf6-127">Oturumu kapatma bağlamının adı</span><span class="sxs-lookup"><span data-stu-id="32bf6-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bf6-128">-DefaultProfile</span></span>
<span data-ttu-id="32bf6-129">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="32bf6-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32bf6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32bf6-130">-InputObject</span></span>
<span data-ttu-id="32bf6-131">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="32bf6-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-132">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="32bf6-132">-Scope</span></span>
<span data-ttu-id="32bf6-133">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="32bf6-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="32bf6-134">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="32bf6-134">-TenantId</span></span>
<span data-ttu-id="32bf6-135">Kiracı kimliği (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="32bf6-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-136">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="32bf6-136">-Username</span></span>
<span data-ttu-id="32bf6-137">' ' Formunun Kullanıcı adı user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="32bf6-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bf6-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="32bf6-138">-Confirm</span></span>
<span data-ttu-id="32bf6-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32bf6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bf6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bf6-140">-WhatIf</span></span>
<span data-ttu-id="32bf6-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32bf6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32bf6-142">Cmdlet yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="32bf6-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="32bf6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bf6-143">CommonParameters</span></span>
<span data-ttu-id="32bf6-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32bf6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bf6-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32bf6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bf6-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32bf6-146">INPUTS</span></span>

### <span data-ttu-id="32bf6-147">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="32bf6-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="32bf6-148">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="32bf6-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="32bf6-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32bf6-149">OUTPUTS</span></span>

### <span data-ttu-id="32bf6-150">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="32bf6-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="32bf6-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32bf6-151">NOTES</span></span>

## <span data-ttu-id="32bf6-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32bf6-152">RELATED LINKS</span></span>
