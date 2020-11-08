---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275347"
---
# <span data-ttu-id="4292a-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="4292a-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="4292a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4292a-102">SYNOPSIS</span></span>
<span data-ttu-id="4292a-103">Belirtilen abonelik, kaynak grubu ve kaynak adı için SAP monitörünü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4292a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4292a-104">SYNTAX</span></span>

### <span data-ttu-id="4292a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4292a-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4292a-106">Al</span><span class="sxs-lookup"><span data-stu-id="4292a-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4292a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4292a-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4292a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4292a-108">DESCRIPTION</span></span>
<span data-ttu-id="4292a-109">Belirtilen abonelik, kaynak grubu ve kaynak adı için SAP monitörünü özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4292a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4292a-110">EXAMPLES</span></span>

### <span data-ttu-id="4292a-111">Örnek 1: aboneliğin altındaki tüm SAP izleyicilerini alma</span><span class="sxs-lookup"><span data-stu-id="4292a-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4292a-112">Bu komut, bir aboneliğin altında SAP monitörleri alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="4292a-113">Örnek 2: ada göre SAP izlemesi alma</span><span class="sxs-lookup"><span data-stu-id="4292a-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4292a-114">Bu komut, SAP monitörünü ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="4292a-115">Örnek 3: nesneye göre SAP izlemesi edinme</span><span class="sxs-lookup"><span data-stu-id="4292a-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4292a-116">Bu komut, bir SAP monitörünü nesneye alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="4292a-117">Örnek 4: ardışık düzene göre SAP izlemesi edinme</span><span class="sxs-lookup"><span data-stu-id="4292a-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4292a-118">Bu komut, ardışık düzene göre SAP izleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="4292a-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="4292a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4292a-119">PARAMETERS</span></span>

### <span data-ttu-id="4292a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4292a-120">-DefaultProfile</span></span>
<span data-ttu-id="4292a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4292a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4292a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4292a-122">-InputObject</span></span>
<span data-ttu-id="4292a-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4292a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4292a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4292a-124">-Name</span></span>
<span data-ttu-id="4292a-125">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4292a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4292a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4292a-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4292a-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4292a-128">-SubscriptionId</span></span>
<span data-ttu-id="4292a-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4292a-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4292a-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4292a-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4292a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4292a-131">CommonParameters</span></span>
<span data-ttu-id="4292a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4292a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4292a-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4292a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4292a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4292a-134">INPUTS</span></span>

### <span data-ttu-id="4292a-135">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="4292a-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="4292a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4292a-136">OUTPUTS</span></span>

### <span data-ttu-id="4292a-137">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="4292a-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="4292a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4292a-138">NOTES</span></span>

<span data-ttu-id="4292a-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4292a-139">ALIASES</span></span>

<span data-ttu-id="4292a-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4292a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4292a-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4292a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4292a-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4292a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4292a-143">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4292a-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4292a-144">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4292a-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4292a-145">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="4292a-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="4292a-146">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="4292a-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="4292a-147">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="4292a-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4292a-149">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="4292a-150">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="4292a-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="4292a-151">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="4292a-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="4292a-152">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="4292a-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="4292a-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4292a-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4292a-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4292a-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4292a-155">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="4292a-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="4292a-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4292a-156">RELATED LINKS</span></span>

