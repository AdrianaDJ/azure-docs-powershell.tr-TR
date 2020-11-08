---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275058"
---
# <span data-ttu-id="89d0f-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="89d0f-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="89d0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="89d0f-103">Özel kaynak sağlayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="89d0f-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="89d0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89d0f-104">SYNTAX</span></span>

### <span data-ttu-id="89d0f-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89d0f-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89d0f-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="89d0f-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89d0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="89d0f-108">Özel kaynak sağlayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="89d0f-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="89d0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89d0f-109">EXAMPLES</span></span>

### <span data-ttu-id="89d0f-110">Örnek 1: özel bir sağlayıcıyı kaldırma.</span><span class="sxs-lookup"><span data-stu-id="89d0f-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="89d0f-111">Özel sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="89d0f-111">Remove a custom provider</span></span>

### <span data-ttu-id="89d0f-112">Örnek 2: geçiş ile özel bir sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="89d0f-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="89d0f-113">Başarı veya başarısızlığı göstermek için geçiş özelliğini kullanarak özel bir sağlayıcıyı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="89d0f-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="89d0f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89d0f-114">PARAMETERS</span></span>

### <span data-ttu-id="89d0f-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="89d0f-115">-AsJob</span></span>
<span data-ttu-id="89d0f-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="89d0f-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d0f-117">-DefaultProfile</span></span>
<span data-ttu-id="89d0f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89d0f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89d0f-119">-InputObject</span></span>
<span data-ttu-id="89d0f-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89d0f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="89d0f-121">-Name</span></span>
<span data-ttu-id="89d0f-122">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89d0f-123">-NoWait</span></span>
<span data-ttu-id="89d0f-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="89d0f-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89d0f-125">-PassThru</span></span>
<span data-ttu-id="89d0f-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="89d0f-126">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d0f-127">-ResourceGroupName</span></span>
<span data-ttu-id="89d0f-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="89d0f-129">-SubscriptionId</span></span>
<span data-ttu-id="89d0f-130">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="89d0f-130">The Azure subscription ID.</span></span>
<span data-ttu-id="89d0f-131">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="89d0f-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d0f-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="89d0f-132">-Confirm</span></span>
<span data-ttu-id="89d0f-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89d0f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d0f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d0f-134">-WhatIf</span></span>
<span data-ttu-id="89d0f-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89d0f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d0f-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89d0f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d0f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d0f-137">CommonParameters</span></span>
<span data-ttu-id="89d0f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89d0f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d0f-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89d0f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d0f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89d0f-140">INPUTS</span></span>

### <span data-ttu-id="89d0f-141">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. ıcustomprovidersıdentity</span><span class="sxs-lookup"><span data-stu-id="89d0f-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="89d0f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89d0f-142">OUTPUTS</span></span>

### <span data-ttu-id="89d0f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89d0f-143">System.Boolean</span></span>

## <span data-ttu-id="89d0f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89d0f-144">NOTES</span></span>

<span data-ttu-id="89d0f-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="89d0f-145">ALIASES</span></span>

<span data-ttu-id="89d0f-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="89d0f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89d0f-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="89d0f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89d0f-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89d0f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89d0f-149">INPUTOBJECT <ICustomProvidersIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="89d0f-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89d0f-150">`[AssociationName <String>]`: İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="89d0f-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="89d0f-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89d0f-152">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="89d0f-153">`[ResourceProviderName <String>]`: Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="89d0f-154">`[Scope <String>]`: İlişkinin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="89d0f-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="89d0f-155">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="89d0f-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="89d0f-156">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="89d0f-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="89d0f-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89d0f-157">RELATED LINKS</span></span>

