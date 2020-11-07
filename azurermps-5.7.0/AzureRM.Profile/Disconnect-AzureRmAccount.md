---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764018"
---
# <span data-ttu-id="fb97d-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fb97d-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="fb97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb97d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb97d-103">Bağlı bir Azure hesabının bağlantısını keser ve bu hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb97d-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb97d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb97d-104">SYNTAX</span></span>

### <span data-ttu-id="fb97d-105">ContextName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb97d-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb97d-106">Desteklenmeyen</span><span class="sxs-lookup"><span data-stu-id="fb97d-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb97d-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fb97d-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb97d-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fb97d-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb97d-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="fb97d-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb97d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb97d-110">DESCRIPTION</span></span>
<span data-ttu-id="fb97d-111">Disconnect-AzureRmAccount cmdlet 'i bağlı bir Azure hesabının bağlantısını keser ve bu Firmayla ilişkili tüm kimlik bilgilerini ve bağlamları (abonelik ve kiracı bilgileri) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb97d-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="fb97d-112">Bu cmdlet 'i çalıştırdıktan sonra Connect-AzureRmAccount kullanarak yeniden oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fb97d-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="fb97d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb97d-113">EXAMPLES</span></span>

### <span data-ttu-id="fb97d-114">Geçerli hesabın oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="fb97d-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="fb97d-115">Geçerli içerikle ilişkili Azure hesabından oturum açar.</span><span class="sxs-lookup"><span data-stu-id="fb97d-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="fb97d-116">Belirli bir içerikle ilişkili hesabın oturumu kapatma</span><span class="sxs-lookup"><span data-stu-id="fb97d-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="fb97d-117">Verilen içerikle ilişkili hesabı (' çalışma ' adlı) günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fb97d-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="fb97d-118">Bu, ' CurrentUser ' kapsamını kullandığı için tüm kimlik bilgileri ve bağlamlar kalıcı olarak silinecektir.</span><span class="sxs-lookup"><span data-stu-id="fb97d-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="fb97d-119">Belirli bir kullanıcının oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="fb97d-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="fb97d-120">' user1@contoso.org ' Kullanıcıyı-tüm kimlik bilgilerini ve bu kullanıcıyla ilişkili tüm bağlamları günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fb97d-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="fb97d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb97d-121">PARAMETERS</span></span>

### <span data-ttu-id="fb97d-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fb97d-122">-ApplicationId</span></span>
<span data-ttu-id="fb97d-123">ServicePrincipal ID (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="fb97d-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="fb97d-124">-AzureContext</span></span>
<span data-ttu-id="fb97d-125">Dan</span><span class="sxs-lookup"><span data-stu-id="fb97d-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="fb97d-126">-ContextName</span></span>
<span data-ttu-id="fb97d-127">Oturumu kapatma bağlamının adı</span><span class="sxs-lookup"><span data-stu-id="fb97d-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb97d-128">-DefaultProfile</span></span>
<span data-ttu-id="fb97d-129">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb97d-129">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb97d-130">-InputObject</span></span>
<span data-ttu-id="fb97d-131">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb97d-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-132">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="fb97d-132">-Scope</span></span>
<span data-ttu-id="fb97d-133">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="fb97d-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-134">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="fb97d-134">-TenantId</span></span>
<span data-ttu-id="fb97d-135">Kiracı kimliği (genel benzersiz kimlik)</span><span class="sxs-lookup"><span data-stu-id="fb97d-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-136">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="fb97d-136">-Username</span></span>
<span data-ttu-id="fb97d-137">' ' Formunun Kullanıcı adı user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="fb97d-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb97d-138">-Confirm</span></span>
<span data-ttu-id="fb97d-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb97d-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb97d-140">-WhatIf</span></span>
<span data-ttu-id="fb97d-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb97d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb97d-142">Cmdlet yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="fb97d-142">The cmdlet is not executed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb97d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb97d-143">CommonParameters</span></span>
<span data-ttu-id="fb97d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb97d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb97d-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb97d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb97d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb97d-146">INPUTS</span></span>

### <span data-ttu-id="fb97d-147">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fb97d-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="fb97d-148">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fb97d-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="fb97d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb97d-149">OUTPUTS</span></span>

### <span data-ttu-id="fb97d-150">Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fb97d-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="fb97d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb97d-151">NOTES</span></span>

## <span data-ttu-id="fb97d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb97d-152">RELATED LINKS</span></span>
