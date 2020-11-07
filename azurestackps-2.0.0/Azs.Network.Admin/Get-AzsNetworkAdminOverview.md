---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935994"
---
# <span data-ttu-id="8e948-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="8e948-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="8e948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e948-102">SYNOPSIS</span></span>
<span data-ttu-id="8e948-103">Ağ kaynağı sağlayıcısının durumuna genel bakış.</span><span class="sxs-lookup"><span data-stu-id="8e948-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="8e948-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e948-104">SYNTAX</span></span>

### <span data-ttu-id="8e948-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e948-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e948-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="8e948-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e948-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e948-107">DESCRIPTION</span></span>
<span data-ttu-id="8e948-108">Ağ kaynağı sağlayıcısının durumuna genel bakış.</span><span class="sxs-lookup"><span data-stu-id="8e948-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="8e948-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e948-109">EXAMPLES</span></span>

### <span data-ttu-id="8e948-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e948-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="8e948-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e948-111">PARAMETERS</span></span>

### <span data-ttu-id="8e948-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e948-112">-DefaultProfile</span></span>
<span data-ttu-id="8e948-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e948-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e948-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e948-114">-InputObject</span></span>
<span data-ttu-id="8e948-115">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e948-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8e948-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8e948-116">-SubscriptionId</span></span>
<span data-ttu-id="8e948-117">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="8e948-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e948-118">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e948-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e948-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e948-119">CommonParameters</span></span>
<span data-ttu-id="8e948-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e948-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e948-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e948-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e948-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e948-122">INPUTS</span></span>

### <span data-ttu-id="8e948-123">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. ınetworkadminıdentity</span><span class="sxs-lookup"><span data-stu-id="8e948-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="8e948-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e948-124">OUTPUTS</span></span>

### <span data-ttu-id="8e948-125">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıadminoverview</span><span class="sxs-lookup"><span data-stu-id="8e948-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="8e948-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e948-126">NOTES</span></span>

<span data-ttu-id="8e948-127">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8e948-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e948-128">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e948-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e948-129">INPUTOBJECT <INetworkAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8e948-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e948-130">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8e948-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e948-131">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="8e948-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8e948-132">`[ResourceName <String>]`: Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="8e948-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="8e948-133">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="8e948-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e948-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e948-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e948-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e948-135">RELATED LINKS</span></span>

