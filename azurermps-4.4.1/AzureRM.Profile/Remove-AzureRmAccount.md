---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590675"
---
# <span data-ttu-id="212bc-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="212bc-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="212bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="212bc-102">SYNOPSIS</span></span>
<span data-ttu-id="212bc-103">Belirtilen hesap ile ilişkili tüm kimlik bilgilerini ve bağlamları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="212bc-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="212bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="212bc-104">SYNTAX</span></span>

### <span data-ttu-id="212bc-105">ContextName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="212bc-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bc-106">Desteklenmeyen</span><span class="sxs-lookup"><span data-stu-id="212bc-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bc-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="212bc-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bc-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="212bc-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bc-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="212bc-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="212bc-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="212bc-110">DESCRIPTION</span></span>
<span data-ttu-id="212bc-111">Verilen hesapla ilişkili tüm kimlik bilgilerini ve bağlamları (abonelik ve kiracı bilgileri) kaldırın.</span><span class="sxs-lookup"><span data-stu-id="212bc-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="212bc-112">Bu cmdlet 'i çalıştırdıktan sonra Add-AzureRmAccount kullanarak yeniden oturum açmanız gerekir</span><span class="sxs-lookup"><span data-stu-id="212bc-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="212bc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="212bc-113">EXAMPLES</span></span>

### <span data-ttu-id="212bc-114">Geçerli hesabı kapatma</span><span class="sxs-lookup"><span data-stu-id="212bc-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="212bc-115">Geçerli içerikle ilişkili hesabı günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="212bc-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="212bc-116">Belirli bir içerikle ilişkili hesabı kapatma</span><span class="sxs-lookup"><span data-stu-id="212bc-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="212bc-117">Verilen içerikle ilişkili hesabı (' çalışma ' adlı) günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="212bc-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="212bc-118">Bu, ' CurrentUser ' kapsamını kullandığı için tüm kimlik bilgileri ve bağlamlar kalıcı olarak silinecektir.</span><span class="sxs-lookup"><span data-stu-id="212bc-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="212bc-119">Belirli bir kullanıcının oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="212bc-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="212bc-120">' user1@contoso.org ' Kullanıcıyı-tüm kimlik bilgilerini ve bu kullanıcıyla ilişkili tüm bağlamları günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="212bc-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="212bc-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="212bc-121">PARAMETERS</span></span>

### <span data-ttu-id="212bc-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="212bc-122">-ApplicationId</span></span>
<span data-ttu-id="212bc-123">ServicePrincipal ID (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="212bc-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="212bc-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="212bc-124">-AzureContext</span></span>
<span data-ttu-id="212bc-125">Dan</span><span class="sxs-lookup"><span data-stu-id="212bc-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="212bc-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="212bc-126">-ContextName</span></span>
<span data-ttu-id="212bc-127">Oturumu kapatma bağlamının adı</span><span class="sxs-lookup"><span data-stu-id="212bc-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="212bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212bc-128">-DefaultProfile</span></span>
<span data-ttu-id="212bc-129">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="212bc-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="212bc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="212bc-130">-InputObject</span></span>
<span data-ttu-id="212bc-131">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="212bc-131">The account object to remove</span></span>

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

### <span data-ttu-id="212bc-132">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="212bc-132">-Scope</span></span>
<span data-ttu-id="212bc-133">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="212bc-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="212bc-134">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="212bc-134">-TenantId</span></span>
<span data-ttu-id="212bc-135">Kiracı kimliği (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="212bc-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="212bc-136">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="212bc-136">-Username</span></span>
<span data-ttu-id="212bc-137">' ' Formunun Kullanıcı adı user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="212bc-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="212bc-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="212bc-138">-Confirm</span></span>
<span data-ttu-id="212bc-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="212bc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212bc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212bc-140">-WhatIf</span></span>
<span data-ttu-id="212bc-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="212bc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212bc-142">Cmdlet yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="212bc-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="212bc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212bc-143">CommonParameters</span></span>
<span data-ttu-id="212bc-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="212bc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212bc-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="212bc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212bc-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="212bc-146">INPUTS</span></span>

### <span data-ttu-id="212bc-147">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="212bc-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="212bc-148">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="212bc-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="212bc-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="212bc-149">OUTPUTS</span></span>

### <span data-ttu-id="212bc-150">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="212bc-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="212bc-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="212bc-151">NOTES</span></span>

## <span data-ttu-id="212bc-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="212bc-152">RELATED LINKS</span></span>

