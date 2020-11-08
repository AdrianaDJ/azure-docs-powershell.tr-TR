---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267930"
---
# <span data-ttu-id="c81ba-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="c81ba-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="c81ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c81ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ba-103">Özel bulutu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-103">Update a private cloud</span></span>

## <span data-ttu-id="c81ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c81ba-104">SYNTAX</span></span>

### <span data-ttu-id="c81ba-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c81ba-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c81ba-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="c81ba-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c81ba-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c81ba-107">DESCRIPTION</span></span>
<span data-ttu-id="c81ba-108">Özel bulutu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-108">Update a private cloud</span></span>

## <span data-ttu-id="c81ba-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c81ba-109">EXAMPLES</span></span>

### <span data-ttu-id="c81ba-110">Örnek 1: özel bulutun ada göre boyutunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="c81ba-111">Özel bulutun adını adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="c81ba-112">Örnek 2: özel bulutun giriş nesnesine göre boyutunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="c81ba-113">Özel bulutun giriş nesnesine göre boyutunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c81ba-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="c81ba-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c81ba-114">PARAMETERS</span></span>

### <span data-ttu-id="c81ba-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c81ba-115">-AsJob</span></span>
<span data-ttu-id="c81ba-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c81ba-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c81ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ba-117">-DefaultProfile</span></span>
<span data-ttu-id="c81ba-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c81ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81ba-119">-Identitysource</span><span class="sxs-lookup"><span data-stu-id="c81ba-119">-IdentitySource</span></span>
<span data-ttu-id="c81ba-120">vCenter tekli oturum açma kimlik kaynakları oluşturmak Için, ıDENTITYSOURCE Properties için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c81ba-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c81ba-121">-InputObject</span></span>
<span data-ttu-id="c81ba-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c81ba-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="c81ba-123">-Internet</span></span>
<span data-ttu-id="c81ba-124">İnternet bağlantısı etkinleştirildi veya devre dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c81ba-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="c81ba-125">-ManagementClusterSize</span></span>
<span data-ttu-id="c81ba-126">Küme boyutu</span><span class="sxs-lookup"><span data-stu-id="c81ba-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c81ba-127">-Name</span></span>
<span data-ttu-id="c81ba-128">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c81ba-129">-NoWait</span></span>
<span data-ttu-id="c81ba-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c81ba-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c81ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="c81ba-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c81ba-132">The name of the resource group.</span></span>
<span data-ttu-id="c81ba-133">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c81ba-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c81ba-134">-SubscriptionId</span></span>
<span data-ttu-id="c81ba-135">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c81ba-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c81ba-136">-Tag</span></span>
<span data-ttu-id="c81ba-137">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c81ba-137">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81ba-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="c81ba-138">-Confirm</span></span>
<span data-ttu-id="c81ba-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c81ba-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ba-140">-WhatIf</span></span>
<span data-ttu-id="c81ba-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c81ba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ba-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c81ba-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ba-143">CommonParameters</span></span>
<span data-ttu-id="c81ba-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c81ba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ba-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c81ba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ba-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c81ba-146">INPUTS</span></span>

### <span data-ttu-id="c81ba-147">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="c81ba-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="c81ba-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c81ba-148">OUTPUTS</span></span>

### <span data-ttu-id="c81ba-149">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="c81ba-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="c81ba-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c81ba-150">NOTES</span></span>

<span data-ttu-id="c81ba-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c81ba-151">ALIASES</span></span>

<span data-ttu-id="c81ba-152">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c81ba-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c81ba-153">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c81ba-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c81ba-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c81ba-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c81ba-155">IDENTITYSOURCE <ııdentitysource [] >: vCenter tek oturum açma kimlik kaynakları</span><span class="sxs-lookup"><span data-stu-id="c81ba-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="c81ba-156">`[Alias <String>]`: Etki alanının NetBIOS adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="c81ba-157">`[BaseGroupDn <String>]`: Gruplar için temel ayırt edici ad</span><span class="sxs-lookup"><span data-stu-id="c81ba-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="c81ba-158">`[BaseUserDn <String>]`: Kullanıcılar için temel ayırt edici ad</span><span class="sxs-lookup"><span data-stu-id="c81ba-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="c81ba-159">`[Domain <String>]`: Etki alanının DNS adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="c81ba-160">`[Name <String>]`: Kimlik kaynağının adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="c81ba-161">`[Password <String>]`: Kullanıcı ve gruplar için temel DN 'ye en az salt okunur erişim içeren Active Directory kullanıcısının parolası.</span><span class="sxs-lookup"><span data-stu-id="c81ba-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="c81ba-162">`[PrimaryServer <String>]`: Birincil sunucu URL 'SI</span><span class="sxs-lookup"><span data-stu-id="c81ba-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="c81ba-163">`[SecondaryServer <String>]`: İkincil sunucu URL 'SI</span><span class="sxs-lookup"><span data-stu-id="c81ba-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="c81ba-164">`[Ssl <SslEnum?>]`: SSL sertifikası (LDAPS) kullanarak LDAP iletişimini koruma</span><span class="sxs-lookup"><span data-stu-id="c81ba-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="c81ba-165">`[Username <String>]`: Kullanıcılar ve grup için temel DN 'ye en az salt okunur erişim içeren bir Active Directory kullanıcısının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c81ba-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="c81ba-166">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c81ba-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c81ba-167">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="c81ba-168">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="c81ba-169">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="c81ba-170">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c81ba-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c81ba-171">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="c81ba-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="c81ba-172">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="c81ba-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="c81ba-173">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c81ba-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c81ba-174">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c81ba-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="c81ba-175">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c81ba-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="c81ba-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c81ba-176">RELATED LINKS</span></span>

