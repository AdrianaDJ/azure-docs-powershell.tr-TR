---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279940"
---
# <span data-ttu-id="39221-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="39221-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="39221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39221-102">SYNOPSIS</span></span>
<span data-ttu-id="39221-103">Bir SignalR hizmetinin ağ ACL 'sini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="39221-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="39221-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39221-104">SYNTAX</span></span>

### <span data-ttu-id="39221-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39221-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39221-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="39221-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39221-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="39221-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39221-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="39221-108">DESCRIPTION</span></span>
<span data-ttu-id="39221-109">Varsayılan eylem ve genel ve özel bağlantı için ağ ACL 'Leri de içinde olmak üzere bir SignalR hizmetinin ağ ACL 'sini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="39221-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="39221-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39221-110">EXAMPLES</span></span>

### <span data-ttu-id="39221-111">Genel ağ için restapi, istemc</span><span class="sxs-lookup"><span data-stu-id="39221-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="39221-112">Özel uç nokta bağlantısı için istemci bağlantısına ve sunucu bağlantısına izin verme</span><span class="sxs-lookup"><span data-stu-id="39221-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="39221-113">Ortak ağ ve özel uç nokta bağlantısı için istemci bağlantısını reddetme</span><span class="sxs-lookup"><span data-stu-id="39221-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="39221-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39221-114">PARAMETERS</span></span>

### <span data-ttu-id="39221-115">-İzin ver</span><span class="sxs-lookup"><span data-stu-id="39221-115">-Allow</span></span>
<span data-ttu-id="39221-116">İzin verilen ağ EDL 'Leri</span><span class="sxs-lookup"><span data-stu-id="39221-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="39221-117">-AsJob</span></span>
<span data-ttu-id="39221-118">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="39221-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="39221-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="39221-119">-DefaultAction</span></span>
<span data-ttu-id="39221-120">SignalR ağ ACL 'lerin varsayılan eylemi, izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="39221-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="39221-121">Ağ ACL 'Lerini reddetmenize veya ağ ACL 'Lerine izin verip vermemeyeceğine karar verir.</span><span class="sxs-lookup"><span data-stu-id="39221-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="39221-122">Örneğin, varsayılan eylem izin verişimizde, yalnızca Deny ACL 'Leri önemlidir.</span><span class="sxs-lookup"><span data-stu-id="39221-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39221-123">-DefaultProfile</span></span>
<span data-ttu-id="39221-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39221-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="39221-125">-Deny</span></span>
<span data-ttu-id="39221-126">Reddedilen ağ ACL 'Leri</span><span class="sxs-lookup"><span data-stu-id="39221-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39221-127">-InputObject</span></span>
<span data-ttu-id="39221-128">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="39221-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39221-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="39221-129">-Name</span></span>
<span data-ttu-id="39221-130">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="39221-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="39221-131">-PrivateEndpointName</span></span>
<span data-ttu-id="39221-132">Güncelleştirilecek özel uç noktalarının adları</span><span class="sxs-lookup"><span data-stu-id="39221-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="39221-133">-PublicNetwork</span></span>
<span data-ttu-id="39221-134">Ortak ağ ACL 'Lerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="39221-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="39221-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39221-135">-ResourceGroupName</span></span>
<span data-ttu-id="39221-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="39221-136">The resource group name.</span></span>
<span data-ttu-id="39221-137">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="39221-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39221-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="39221-138">-ResourceId</span></span>
<span data-ttu-id="39221-139">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="39221-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39221-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="39221-140">-Confirm</span></span>
<span data-ttu-id="39221-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39221-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39221-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39221-142">-WhatIf</span></span>
<span data-ttu-id="39221-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39221-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39221-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39221-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39221-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39221-145">CommonParameters</span></span>
<span data-ttu-id="39221-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39221-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39221-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39221-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39221-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39221-148">INPUTS</span></span>

### <span data-ttu-id="39221-149">System. String</span><span class="sxs-lookup"><span data-stu-id="39221-149">System.String</span></span>

## <span data-ttu-id="39221-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39221-150">OUTPUTS</span></span>

### <span data-ttu-id="39221-151">Microsoft. Azure. Commands. SignalR. modeller. Pssignalrnetworkcacls</span><span class="sxs-lookup"><span data-stu-id="39221-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="39221-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39221-152">NOTES</span></span>

## <span data-ttu-id="39221-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39221-153">RELATED LINKS</span></span>
