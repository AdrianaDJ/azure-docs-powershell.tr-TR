---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268860"
---
# <span data-ttu-id="60aee-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="60aee-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="60aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aee-102">SYNOPSIS</span></span>
<span data-ttu-id="60aee-103">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için Sağlayıcı örneğinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="60aee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60aee-104">SYNTAX</span></span>

### <span data-ttu-id="60aee-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60aee-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60aee-106">Al</span><span class="sxs-lookup"><span data-stu-id="60aee-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60aee-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="60aee-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="60aee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60aee-108">DESCRIPTION</span></span>
<span data-ttu-id="60aee-109">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için Sağlayıcı örneğinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="60aee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60aee-110">EXAMPLES</span></span>

### <span data-ttu-id="60aee-111">Örnek 1: SAP İzleyicisi altındaki tüm örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="60aee-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="60aee-112">Bu komut SAP İzleyicisi altındaki tüm örnekleri alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="60aee-113">Örnek 2: ada göre SAP izleme örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="60aee-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="60aee-114">Bu komut SAP monitörü 'nün bir örneğini ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="60aee-115">Örnek 3: nesne tarafından SAP izleme örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="60aee-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="60aee-116">Bu komut, nesne tarafından SAP izleme örnekleri alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="60aee-117">Örnek 4: ardışık düzene göre SAP izleme örnekleri alma</span><span class="sxs-lookup"><span data-stu-id="60aee-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="60aee-118">Bu komut, bir SAP izleme örneğini ardışık düzene göre alır.</span><span class="sxs-lookup"><span data-stu-id="60aee-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="60aee-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60aee-119">PARAMETERS</span></span>

### <span data-ttu-id="60aee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aee-120">-DefaultProfile</span></span>
<span data-ttu-id="60aee-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60aee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60aee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60aee-122">-InputObject</span></span>
<span data-ttu-id="60aee-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60aee-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60aee-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="60aee-124">-Name</span></span>
<span data-ttu-id="60aee-125">Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aee-126">-ResourceGroupName</span></span>
<span data-ttu-id="60aee-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aee-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="60aee-128">-SapMonitorName</span></span>
<span data-ttu-id="60aee-129">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aee-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="60aee-130">-SubscriptionId</span></span>
<span data-ttu-id="60aee-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60aee-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60aee-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60aee-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60aee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aee-133">CommonParameters</span></span>
<span data-ttu-id="60aee-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60aee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aee-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60aee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aee-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60aee-136">INPUTS</span></span>

### <span data-ttu-id="60aee-137">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="60aee-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="60aee-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60aee-138">OUTPUTS</span></span>

### <span data-ttu-id="60aee-139">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="60aee-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="60aee-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60aee-140">NOTES</span></span>

<span data-ttu-id="60aee-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="60aee-141">ALIASES</span></span>

<span data-ttu-id="60aee-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="60aee-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60aee-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="60aee-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60aee-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60aee-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60aee-145">INPUTOBJECT <IHanaOnAzureIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="60aee-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60aee-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="60aee-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60aee-147">`[Location <String>]`: Silinen kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="60aee-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="60aee-148">`[OperationKind <AccessPolicyUpdateKind?>]`: İşlemin adı</span><span class="sxs-lookup"><span data-stu-id="60aee-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="60aee-149">`[ProviderInstanceName <String>]`: Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="60aee-150">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="60aee-151">`[ResourceName <String>]`: Kimlik kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="60aee-152">`[SapMonitorName <String>]`: SAP izleme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="60aee-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="60aee-153">`[Scope <String>]`: Kaynağın kaynak sağlayıcısı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="60aee-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="60aee-154">Yönetilen kimlikler tarafından genişletilen üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="60aee-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="60aee-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60aee-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="60aee-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60aee-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="60aee-157">`[VaultName <String>]`: Kasaın adı</span><span class="sxs-lookup"><span data-stu-id="60aee-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="60aee-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60aee-158">RELATED LINKS</span></span>

