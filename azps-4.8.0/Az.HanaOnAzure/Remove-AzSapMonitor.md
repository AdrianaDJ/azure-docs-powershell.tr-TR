---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109613"
---
# <span data-ttu-id="20752-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="20752-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="20752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20752-102">SYNOPSIS</span></span>
<span data-ttu-id="20752-103">Belirtilen abonelikle, kaynak grubuyla ve monitör adıyla bir SAP izleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="20752-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="20752-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20752-104">SYNTAX</span></span>

### <span data-ttu-id="20752-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20752-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20752-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="20752-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20752-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20752-107">DESCRIPTION</span></span>
<span data-ttu-id="20752-108">Belirtilen abonelikle, kaynak grubuyla ve monitör adıyla bir SAP izleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="20752-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="20752-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20752-109">EXAMPLES</span></span>

### <span data-ttu-id="20752-110">Örnek 1: ada göre SAP izleyicisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="20752-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="20752-111">Bu komut SAP monitörünü ada göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20752-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="20752-112">Örnek 2: nesne bazında SAP monitörünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="20752-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="20752-113">Bu komut, SAP monitörünü nesneye göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20752-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="20752-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20752-114">PARAMETERS</span></span>

### <span data-ttu-id="20752-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="20752-115">-AsJob</span></span>
<span data-ttu-id="20752-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="20752-116">Run the command as a job</span></span>

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

### <span data-ttu-id="20752-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20752-117">-DefaultProfile</span></span>
<span data-ttu-id="20752-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20752-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20752-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20752-119">-InputObject</span></span>
<span data-ttu-id="20752-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20752-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20752-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="20752-121">-Name</span></span>
<span data-ttu-id="20752-122">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="20752-122">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="20752-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20752-123">-NoWait</span></span>
<span data-ttu-id="20752-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="20752-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="20752-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20752-125">-PassThru</span></span>
<span data-ttu-id="20752-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="20752-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="20752-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20752-127">-ResourceGroupName</span></span>
<span data-ttu-id="20752-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="20752-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="20752-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="20752-129">-SubscriptionId</span></span>
<span data-ttu-id="20752-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20752-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="20752-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20752-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="20752-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="20752-132">-Confirm</span></span>
<span data-ttu-id="20752-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20752-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20752-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20752-134">-WhatIf</span></span>
<span data-ttu-id="20752-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20752-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20752-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20752-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20752-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20752-137">CommonParameters</span></span>
<span data-ttu-id="20752-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20752-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20752-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="20752-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20752-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20752-140">INPUTS</span></span>

### <span data-ttu-id="20752-141">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="20752-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="20752-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20752-142">OUTPUTS</span></span>

### <span data-ttu-id="20752-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20752-143">System.Boolean</span></span>

## <span data-ttu-id="20752-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20752-144">NOTES</span></span>

<span data-ttu-id="20752-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="20752-145">ALIASES</span></span>

<span data-ttu-id="20752-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="20752-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20752-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="20752-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20752-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20752-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20752-149">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="20752-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20752-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="20752-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20752-151">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="20752-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="20752-152">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="20752-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="20752-153">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="20752-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="20752-154">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="20752-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="20752-155">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="20752-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="20752-156">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="20752-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="20752-157">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="20752-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="20752-158">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="20752-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="20752-159">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20752-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="20752-160">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20752-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="20752-161">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="20752-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="20752-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20752-162">RELATED LINKS</span></span>

