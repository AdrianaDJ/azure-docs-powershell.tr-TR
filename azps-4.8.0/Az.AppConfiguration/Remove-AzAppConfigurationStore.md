---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273729"
---
# <span data-ttu-id="6e4d3-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6e4d3-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="6e4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4d3-103">Yapılandırma deposunu siler.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="6e4d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e4d3-104">SYNTAX</span></span>

### <span data-ttu-id="6e4d3-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e4d3-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e4d3-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6e4d3-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e4d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e4d3-107">DESCRIPTION</span></span>
<span data-ttu-id="6e4d3-108">Yapılandırma deposunu siler.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="6e4d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e4d3-109">EXAMPLES</span></span>

### <span data-ttu-id="6e4d3-110">Örnek 1: uygulama yapılandırma deposunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e4d3-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="6e4d3-111">Bu komut, uygulama yapılandırma deposunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="6e4d3-112">Örnek 2: uygulama yapılandırma deposunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e4d3-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="6e4d3-113">Bu komut, uygulama yapılandırma deposunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="6e4d3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e4d3-114">PARAMETERS</span></span>

### <span data-ttu-id="6e4d3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6e4d3-115">-AsJob</span></span>
<span data-ttu-id="6e4d3-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="6e4d3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6e4d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4d3-117">-DefaultProfile</span></span>
<span data-ttu-id="6e4d3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e4d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e4d3-119">-InputObject</span></span>
<span data-ttu-id="6e4d3-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4d3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e4d3-121">-Name</span></span>
<span data-ttu-id="6e4d3-122">Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="6e4d3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6e4d3-123">-NoWait</span></span>
<span data-ttu-id="6e4d3-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="6e4d3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e4d3-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6e4d3-125">-PassThru</span></span>
<span data-ttu-id="6e4d3-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="6e4d3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6e4d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e4d3-128">Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="6e4d3-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6e4d3-129">-SubscriptionId</span></span>
<span data-ttu-id="6e4d3-130">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="6e4d3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e4d3-131">-Confirm</span></span>
<span data-ttu-id="6e4d3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e4d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e4d3-133">-WhatIf</span></span>
<span data-ttu-id="6e4d3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e4d3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e4d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4d3-136">CommonParameters</span></span>
<span data-ttu-id="6e4d3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4d3-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4d3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e4d3-139">INPUTS</span></span>

### <span data-ttu-id="6e4d3-140">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. ıappconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="6e4d3-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6e4d3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e4d3-141">OUTPUTS</span></span>

### <span data-ttu-id="6e4d3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e4d3-142">System.Boolean</span></span>

## <span data-ttu-id="6e4d3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e4d3-143">NOTES</span></span>

<span data-ttu-id="6e4d3-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6e4d3-144">ALIASES</span></span>

<span data-ttu-id="6e4d3-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6e4d3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e4d3-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e4d3-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e4d3-148">INPUTOBJECT <IAppConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6e4d3-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e4d3-149">`[ConfigStoreName <String>]`: Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6e4d3-150">`[GroupName <String>]`: Özel bağlantı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6e4d3-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6e4d3-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e4d3-152">`[PrivateEndpointConnectionName <String>]`: Özel uç noktası bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="6e4d3-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6e4d3-153">`[ResourceGroupName <String>]`: Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6e4d3-154">`[SubscriptionId <String>]`: Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6e4d3-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6e4d3-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e4d3-155">RELATED LINKS</span></span>

