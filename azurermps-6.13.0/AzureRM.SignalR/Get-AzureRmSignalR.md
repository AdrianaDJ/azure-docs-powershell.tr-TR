---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590843"
---
# <span data-ttu-id="8ecd6-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="8ecd6-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="8ecd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ecd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecd6-103">Belirli bir SignalR hizmeti veya bir kaynak grubundaki tüm SignalR hizmetlerini veya bir aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ecd6-104">SYNTAX</span></span>

### <span data-ttu-id="8ecd6-105">ListSignalRServiceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ecd6-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ecd6-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ecd6-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ecd6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8ecd6-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ecd6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ecd6-108">DESCRIPTION</span></span>
<span data-ttu-id="8ecd6-109">Belirli bir SignalR hizmeti veya bir kaynak grubundaki tüm SignalR hizmetlerini veya bir aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="8ecd6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ecd6-110">EXAMPLES</span></span>

### <span data-ttu-id="8ecd6-111">Aboneliğe tüm SignalR hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="8ecd6-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="8ecd6-112">Kaynak grubundaki tüm SignalR hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="8ecd6-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="8ecd6-113">Belirli bir SignalR hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="8ecd6-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="8ecd6-114">Varsayılan kaynak grubundan belirli bir SignalR hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="8ecd6-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="8ecd6-115">Varsayılan kaynak grubu tarafından ayarlanabilir `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="8ecd6-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="8ecd6-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ecd6-116">PARAMETERS</span></span>

### <span data-ttu-id="8ecd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecd6-117">-DefaultProfile</span></span>
<span data-ttu-id="8ecd6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecd6-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ecd6-119">-Name</span></span>
<span data-ttu-id="8ecd6-120">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-120">SignalR service name.</span></span>

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

### <span data-ttu-id="8ecd6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecd6-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ecd6-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-122">Resource group name.</span></span>

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

### <span data-ttu-id="8ecd6-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8ecd6-123">-ResourceId</span></span>
<span data-ttu-id="8ecd6-124">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="8ecd6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecd6-125">CommonParameters</span></span>
<span data-ttu-id="8ecd6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ecd6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecd6-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecd6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecd6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ecd6-128">INPUTS</span></span>

### <span data-ttu-id="8ecd6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecd6-129">System.String</span></span>
<span data-ttu-id="8ecd6-130">Parametreler: RESOURCEID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ecd6-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="8ecd6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ecd6-131">OUTPUTS</span></span>

### <span data-ttu-id="8ecd6-132">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="8ecd6-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="8ecd6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ecd6-133">NOTES</span></span>

## <span data-ttu-id="8ecd6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ecd6-134">RELATED LINKS</span></span>
