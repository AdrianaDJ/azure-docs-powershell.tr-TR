---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275341"
---
# <span data-ttu-id="65622-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="65622-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="65622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65622-102">SYNOPSIS</span></span>
<span data-ttu-id="65622-103">Belirtilen abonelikle, kaynak grubuyla ve monitör adıyla bir SAP izleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="65622-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="65622-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65622-104">SYNTAX</span></span>

### <span data-ttu-id="65622-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65622-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65622-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="65622-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65622-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="65622-107">DESCRIPTION</span></span>
<span data-ttu-id="65622-108">Belirtilen abonelikle, kaynak grubuyla ve monitör adıyla bir SAP izleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="65622-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="65622-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65622-109">EXAMPLES</span></span>

### <span data-ttu-id="65622-110">Örnek 1: ada göre SAP izleyicisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="65622-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="65622-111">Bu komut SAP monitörünü ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65622-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="65622-112">Örnek 2: nesne bazında SAP monitörünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="65622-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="65622-113">Bu komut, SAP monitörünü nesneye göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65622-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="65622-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65622-114">PARAMETERS</span></span>

### <span data-ttu-id="65622-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="65622-115">-AsJob</span></span>
<span data-ttu-id="65622-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="65622-116">Run the command as a job</span></span>

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

### <span data-ttu-id="65622-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65622-117">-DefaultProfile</span></span>
<span data-ttu-id="65622-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65622-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65622-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65622-119">-InputObject</span></span>
<span data-ttu-id="65622-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65622-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65622-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="65622-121">-Name</span></span>
<span data-ttu-id="65622-122">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="65622-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65622-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="65622-123">-NoWait</span></span>
<span data-ttu-id="65622-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="65622-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="65622-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="65622-125">-PassThru</span></span>
<span data-ttu-id="65622-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="65622-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="65622-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65622-127">-ResourceGroupName</span></span>
<span data-ttu-id="65622-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="65622-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="65622-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="65622-129">-SubscriptionId</span></span>
<span data-ttu-id="65622-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65622-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="65622-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65622-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="65622-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="65622-132">-Confirm</span></span>
<span data-ttu-id="65622-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65622-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65622-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65622-134">-WhatIf</span></span>
<span data-ttu-id="65622-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65622-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65622-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65622-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65622-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65622-137">CommonParameters</span></span>
<span data-ttu-id="65622-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65622-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65622-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65622-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65622-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65622-140">INPUTS</span></span>

### <span data-ttu-id="65622-141">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="65622-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="65622-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65622-142">OUTPUTS</span></span>

### <span data-ttu-id="65622-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65622-143">System.Boolean</span></span>

## <span data-ttu-id="65622-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65622-144">NOTES</span></span>

<span data-ttu-id="65622-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="65622-145">ALIASES</span></span>

<span data-ttu-id="65622-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="65622-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65622-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65622-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65622-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65622-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65622-149">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="65622-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65622-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="65622-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65622-151">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="65622-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="65622-152">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="65622-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="65622-153">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="65622-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="65622-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="65622-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="65622-155">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="65622-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="65622-156">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="65622-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="65622-157">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="65622-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="65622-158">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="65622-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="65622-159">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65622-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="65622-160">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65622-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="65622-161">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="65622-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="65622-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65622-162">RELATED LINKS</span></span>

