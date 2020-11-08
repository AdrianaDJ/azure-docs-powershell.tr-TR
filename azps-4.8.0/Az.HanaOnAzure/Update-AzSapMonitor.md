---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267235"
---
# <span data-ttu-id="dda25-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="dda25-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="dda25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda25-102">SYNOPSIS</span></span>
<span data-ttu-id="dda25-103">Belirtilen abonelik, kaynak grubu ve monitör adı için SAP izlemenin Etiketler alanı düzeltme ekleri.</span><span class="sxs-lookup"><span data-stu-id="dda25-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="dda25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dda25-104">SYNTAX</span></span>

### <span data-ttu-id="dda25-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dda25-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dda25-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="dda25-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dda25-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dda25-107">DESCRIPTION</span></span>
<span data-ttu-id="dda25-108">Belirtilen abonelik, kaynak grubu ve monitör adı için SAP izlemenin Etiketler alanı düzeltme ekleri.</span><span class="sxs-lookup"><span data-stu-id="dda25-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="dda25-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dda25-109">EXAMPLES</span></span>

### <span data-ttu-id="dda25-110">Örnek 1: SAP izleyicisini ada göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="dda25-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="dda25-111">Bu komutlar SAP monitörünü ada göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dda25-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="dda25-112">Örnek 2: bir SAP izleyicisini nesneye göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="dda25-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="dda25-113">Bu komut, bir SAP izleyicisini nesneye göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dda25-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="dda25-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dda25-114">PARAMETERS</span></span>

### <span data-ttu-id="dda25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda25-115">-DefaultProfile</span></span>
<span data-ttu-id="dda25-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dda25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda25-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dda25-117">-InputObject</span></span>
<span data-ttu-id="dda25-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dda25-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dda25-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dda25-119">-Name</span></span>
<span data-ttu-id="dda25-120">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda25-121">-ResourceGroupName</span></span>
<span data-ttu-id="dda25-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="dda25-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dda25-123">-SubscriptionId</span></span>
<span data-ttu-id="dda25-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dda25-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dda25-125">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dda25-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dda25-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dda25-126">-Tag</span></span>
<span data-ttu-id="dda25-127">Kaynağın Etiketler alanı.</span><span class="sxs-lookup"><span data-stu-id="dda25-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="dda25-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="dda25-128">-Confirm</span></span>
<span data-ttu-id="dda25-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dda25-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda25-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda25-130">-WhatIf</span></span>
<span data-ttu-id="dda25-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dda25-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda25-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dda25-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda25-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda25-133">CommonParameters</span></span>
<span data-ttu-id="dda25-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dda25-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda25-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dda25-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda25-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dda25-136">INPUTS</span></span>

### <span data-ttu-id="dda25-137">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="dda25-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="dda25-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dda25-138">OUTPUTS</span></span>

### <span data-ttu-id="dda25-139">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="dda25-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="dda25-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dda25-140">NOTES</span></span>

<span data-ttu-id="dda25-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="dda25-141">ALIASES</span></span>

<span data-ttu-id="dda25-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="dda25-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dda25-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dda25-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dda25-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dda25-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dda25-145">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="dda25-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dda25-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="dda25-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dda25-147">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="dda25-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="dda25-148">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="dda25-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="dda25-149">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="dda25-150">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dda25-151">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="dda25-152">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="dda25-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="dda25-153">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="dda25-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="dda25-154">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="dda25-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="dda25-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dda25-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dda25-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dda25-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dda25-157">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="dda25-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="dda25-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dda25-158">RELATED LINKS</span></span>

