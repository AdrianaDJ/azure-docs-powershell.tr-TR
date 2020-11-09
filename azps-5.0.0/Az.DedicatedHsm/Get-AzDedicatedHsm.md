---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320190"
---
# <span data-ttu-id="b3786-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b3786-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="b3786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3786-102">SYNOPSIS</span></span>
<span data-ttu-id="b3786-103">Belirtilen Azure adanmış HSM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="b3786-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b3786-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3786-104">SYNTAX</span></span>

### <span data-ttu-id="b3786-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3786-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3786-106">Al</span><span class="sxs-lookup"><span data-stu-id="b3786-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3786-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b3786-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3786-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="b3786-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b3786-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3786-109">DESCRIPTION</span></span>
<span data-ttu-id="b3786-110">Belirtilen Azure adanmış HSM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="b3786-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b3786-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3786-111">EXAMPLES</span></span>

### <span data-ttu-id="b3786-112">Örnek 1: bir aboneliğin altındaki tüm adanmış HSM 'yi alma</span><span class="sxs-lookup"><span data-stu-id="b3786-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b3786-113">Bu komut bir aboneliğin altındaki tüm adanmış HSM 'yi alır</span><span class="sxs-lookup"><span data-stu-id="b3786-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="b3786-114">Örnek 2: kaynak grubu altındaki tüm adanmış HSM 'yi alma.</span><span class="sxs-lookup"><span data-stu-id="b3786-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b3786-115">Bu komut, kaynak grubu altındaki tüm adanmış HSM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="b3786-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="b3786-116">Örnek 3: ada göre adanmış bir HSM alma</span><span class="sxs-lookup"><span data-stu-id="b3786-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b3786-117">Bu komut adanmış bir HSM adını alır.</span><span class="sxs-lookup"><span data-stu-id="b3786-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="b3786-118">Örnek 4: nesneye göre adanmış bir HSM alma</span><span class="sxs-lookup"><span data-stu-id="b3786-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b3786-119">Bu komut, adanmış bir HSM nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="b3786-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="b3786-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3786-120">PARAMETERS</span></span>

### <span data-ttu-id="b3786-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3786-121">-DefaultProfile</span></span>
<span data-ttu-id="b3786-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3786-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3786-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3786-123">-InputObject</span></span>
<span data-ttu-id="b3786-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3786-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3786-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3786-125">-Name</span></span>
<span data-ttu-id="b3786-126">Adanmış HSM 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="b3786-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="b3786-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3786-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3786-128">Adanmış HSM 'nin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b3786-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="b3786-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b3786-129">-SubscriptionId</span></span>
<span data-ttu-id="b3786-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="b3786-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3786-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b3786-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3786-132">-Üst</span><span class="sxs-lookup"><span data-stu-id="b3786-132">-Top</span></span>
<span data-ttu-id="b3786-133">Döndürülecek en fazla sonuç sayısı.</span><span class="sxs-lookup"><span data-stu-id="b3786-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3786-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3786-134">CommonParameters</span></span>
<span data-ttu-id="b3786-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3786-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3786-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3786-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3786-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3786-137">INPUTS</span></span>

### <span data-ttu-id="b3786-138">Microsoft. Azure. PowerShell. cmdlet. (".</span><span class="sxs-lookup"><span data-stu-id="b3786-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="b3786-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3786-139">OUTPUTS</span></span>

### <span data-ttu-id="b3786-140">Microsoft. Azure. PowerShell. cmdlet. ayrılmış Atedhsm. modeller. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b3786-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="b3786-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3786-141">NOTES</span></span>

<span data-ttu-id="b3786-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b3786-142">ALIASES</span></span>

<span data-ttu-id="b3786-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b3786-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3786-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b3786-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3786-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3786-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3786-146">INPUTOBJECT <IDedicatedHsmIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b3786-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3786-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b3786-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3786-148">`[Name <String>]`: Adanmış HSM 'nin adı</span><span class="sxs-lookup"><span data-stu-id="b3786-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="b3786-149">`[ResourceGroupName <String>]`: Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b3786-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="b3786-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="b3786-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b3786-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b3786-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b3786-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3786-152">RELATED LINKS</span></span>

