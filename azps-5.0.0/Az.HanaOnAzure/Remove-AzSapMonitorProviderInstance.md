---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277390"
---
# <span data-ttu-id="fc222-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="fc222-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="fc222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc222-102">SYNOPSIS</span></span>
<span data-ttu-id="fc222-103">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için bir sağlayıcı örneği siler.</span><span class="sxs-lookup"><span data-stu-id="fc222-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="fc222-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc222-104">SYNTAX</span></span>

### <span data-ttu-id="fc222-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc222-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fc222-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="fc222-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc222-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc222-107">DESCRIPTION</span></span>
<span data-ttu-id="fc222-108">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için bir sağlayıcı örneği siler.</span><span class="sxs-lookup"><span data-stu-id="fc222-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="fc222-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc222-109">EXAMPLES</span></span>

### <span data-ttu-id="fc222-110">Örnek 1: SAP izleyicisini ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc222-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="fc222-111">Bu komut SAP İzleyicisi örneğini ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc222-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="fc222-112">Örnek 2: SAP monitörü 'nün nesne örneğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc222-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="fc222-113">Bu komut SAP İzleyicisi örneğini nesneye göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc222-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="fc222-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc222-114">PARAMETERS</span></span>

### <span data-ttu-id="fc222-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="fc222-115">-AsJob</span></span>
<span data-ttu-id="fc222-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="fc222-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fc222-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc222-117">-DefaultProfile</span></span>
<span data-ttu-id="fc222-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc222-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc222-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc222-119">-InputObject</span></span>
<span data-ttu-id="fc222-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc222-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fc222-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc222-121">-Name</span></span>
<span data-ttu-id="fc222-122">Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc222-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fc222-123">-NoWait</span></span>
<span data-ttu-id="fc222-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="fc222-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fc222-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc222-125">-PassThru</span></span>
<span data-ttu-id="fc222-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="fc222-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fc222-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc222-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc222-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="fc222-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="fc222-129">-SapMonitorName</span></span>
<span data-ttu-id="fc222-130">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="fc222-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fc222-131">-SubscriptionId</span></span>
<span data-ttu-id="fc222-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fc222-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fc222-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fc222-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fc222-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc222-134">-Confirm</span></span>
<span data-ttu-id="fc222-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc222-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc222-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc222-136">-WhatIf</span></span>
<span data-ttu-id="fc222-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc222-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc222-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc222-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc222-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc222-139">CommonParameters</span></span>
<span data-ttu-id="fc222-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc222-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc222-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fc222-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc222-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc222-142">INPUTS</span></span>

### <span data-ttu-id="fc222-143">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="fc222-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="fc222-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc222-144">OUTPUTS</span></span>

### <span data-ttu-id="fc222-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc222-145">System.Boolean</span></span>

## <span data-ttu-id="fc222-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc222-146">NOTES</span></span>

<span data-ttu-id="fc222-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="fc222-147">ALIASES</span></span>

<span data-ttu-id="fc222-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="fc222-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc222-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fc222-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc222-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc222-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc222-151">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="fc222-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc222-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="fc222-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc222-153">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="fc222-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="fc222-154">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="fc222-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="fc222-155">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="fc222-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="fc222-157">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="fc222-158">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="fc222-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="fc222-159">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="fc222-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="fc222-160">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="fc222-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="fc222-161">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fc222-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fc222-162">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fc222-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fc222-163">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="fc222-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="fc222-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc222-164">RELATED LINKS</span></span>

