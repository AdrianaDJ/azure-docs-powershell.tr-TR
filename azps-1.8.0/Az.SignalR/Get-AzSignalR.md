---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: be286c0a0006f1b8b054f32269bc06dc05bcf515
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759096"
---
# <span data-ttu-id="3d33b-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="3d33b-101">Get-AzSignalR</span></span>

## <span data-ttu-id="3d33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d33b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d33b-103">Belirli bir SignalR hizmeti veya bir kaynak grubundaki tüm SignalR hizmetlerini veya bir aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="3d33b-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="3d33b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d33b-104">SYNTAX</span></span>

### <span data-ttu-id="3d33b-105">ListSignalRServiceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d33b-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d33b-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d33b-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d33b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3d33b-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d33b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d33b-108">DESCRIPTION</span></span>
<span data-ttu-id="3d33b-109">Belirli bir SignalR hizmeti veya bir kaynak grubundaki tüm SignalR hizmetlerini veya bir aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="3d33b-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="3d33b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d33b-110">EXAMPLES</span></span>

### <span data-ttu-id="3d33b-111">Aboneliğe tüm SignalR hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="3d33b-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="3d33b-112">Kaynak grubundaki tüm SignalR hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="3d33b-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="3d33b-113">Belirli bir SignalR hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="3d33b-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="3d33b-114">Varsayılan kaynak grubundan belirli bir SignalR hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="3d33b-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="3d33b-115">Varsayılan kaynak grubu tarafından ayarlanabilir `Set-AzDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="3d33b-115">The default resource group can be set by `Set-AzDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="3d33b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d33b-116">PARAMETERS</span></span>

### <span data-ttu-id="3d33b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d33b-117">-DefaultProfile</span></span>
<span data-ttu-id="3d33b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d33b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d33b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d33b-119">-Name</span></span>
<span data-ttu-id="3d33b-120">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="3d33b-120">SignalR service name.</span></span>

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

### <span data-ttu-id="3d33b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d33b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d33b-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3d33b-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d33b-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d33b-123">-ResourceId</span></span>
<span data-ttu-id="3d33b-124">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d33b-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d33b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d33b-125">CommonParameters</span></span>
<span data-ttu-id="3d33b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d33b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d33b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d33b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d33b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d33b-128">INPUTS</span></span>

### <span data-ttu-id="3d33b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3d33b-129">System.String</span></span>

## <span data-ttu-id="3d33b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d33b-130">OUTPUTS</span></span>

### <span data-ttu-id="3d33b-131">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3d33b-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="3d33b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d33b-132">NOTES</span></span>

## <span data-ttu-id="3d33b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d33b-133">RELATED LINKS</span></span>
