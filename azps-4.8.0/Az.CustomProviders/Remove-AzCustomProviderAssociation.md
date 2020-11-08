---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275059"
---
# <span data-ttu-id="c822c-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="c822c-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="c822c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c822c-102">SYNOPSIS</span></span>
<span data-ttu-id="c822c-103">İlişkiyi silme.</span><span class="sxs-lookup"><span data-stu-id="c822c-103">Delete an association.</span></span>

## <span data-ttu-id="c822c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c822c-104">SYNTAX</span></span>

### <span data-ttu-id="c822c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c822c-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c822c-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c822c-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c822c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c822c-107">DESCRIPTION</span></span>
<span data-ttu-id="c822c-108">İlişkiyi silme.</span><span class="sxs-lookup"><span data-stu-id="c822c-108">Delete an association.</span></span>

## <span data-ttu-id="c822c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c822c-109">EXAMPLES</span></span>

### <span data-ttu-id="c822c-110">Örnek 1: özel bir sağlayıcı ilişkisini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c822c-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="c822c-111">Özel bir sağlayıcı ilişkisini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c822c-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="c822c-112">Örnek 2: boru ile özel bir sağlayıcı ilişkisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c822c-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="c822c-113">Başarı veya başarısızlığı belirtmek için boruları ve geçiş özelliğini kullanarak özel bir sağlayıcı ilişkilendirmesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="c822c-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="c822c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c822c-114">PARAMETERS</span></span>

### <span data-ttu-id="c822c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c822c-115">-AsJob</span></span>
<span data-ttu-id="c822c-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c822c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c822c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c822c-117">-DefaultProfile</span></span>
<span data-ttu-id="c822c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c822c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c822c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c822c-119">-InputObject</span></span>
<span data-ttu-id="c822c-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c822c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c822c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c822c-121">-Name</span></span>
<span data-ttu-id="c822c-122">İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="c822c-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c822c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c822c-123">-NoWait</span></span>
<span data-ttu-id="c822c-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c822c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c822c-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c822c-125">-PassThru</span></span>
<span data-ttu-id="c822c-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c822c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c822c-127">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c822c-127">-Scope</span></span>
<span data-ttu-id="c822c-128">İlişkilendirmenin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="c822c-128">The scope of the association.</span></span>

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

### <span data-ttu-id="c822c-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c822c-129">-Confirm</span></span>
<span data-ttu-id="c822c-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c822c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c822c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c822c-131">-WhatIf</span></span>
<span data-ttu-id="c822c-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c822c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c822c-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c822c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c822c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c822c-134">CommonParameters</span></span>
<span data-ttu-id="c822c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c822c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c822c-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c822c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c822c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c822c-137">INPUTS</span></span>

### <span data-ttu-id="c822c-138">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. ıcustomprovidersıdentity</span><span class="sxs-lookup"><span data-stu-id="c822c-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="c822c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c822c-139">OUTPUTS</span></span>

### <span data-ttu-id="c822c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c822c-140">System.Boolean</span></span>

## <span data-ttu-id="c822c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c822c-141">NOTES</span></span>

<span data-ttu-id="c822c-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c822c-142">ALIASES</span></span>

<span data-ttu-id="c822c-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c822c-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c822c-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c822c-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c822c-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c822c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c822c-146">INPUTOBJECT <ICustomProvidersIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c822c-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c822c-147">`[AssociationName <String>]`: İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="c822c-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="c822c-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c822c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c822c-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c822c-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c822c-150">`[ResourceProviderName <String>]`: Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="c822c-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="c822c-151">`[Scope <String>]`: İlişkinin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="c822c-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="c822c-152">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c822c-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c822c-153">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c822c-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c822c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c822c-154">RELATED LINKS</span></span>

