---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278740"
---
# <span data-ttu-id="d0c84-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d0c84-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d0c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c84-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c84-103">Uzantıyı alma işlemi.</span><span class="sxs-lookup"><span data-stu-id="d0c84-103">The operation to get the extension.</span></span>

## <span data-ttu-id="d0c84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0c84-104">SYNTAX</span></span>

### <span data-ttu-id="d0c84-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d0c84-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d0c84-106">Al</span><span class="sxs-lookup"><span data-stu-id="d0c84-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d0c84-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0c84-107">DESCRIPTION</span></span>
<span data-ttu-id="d0c84-108">Uzantıyı alma işlemi.</span><span class="sxs-lookup"><span data-stu-id="d0c84-108">The operation to get the extension.</span></span>

## <span data-ttu-id="d0c84-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0c84-109">EXAMPLES</span></span>

### <span data-ttu-id="d0c84-110">Örnek 1: bir makinenin tüm uzantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="d0c84-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="d0c84-111">Belirli bir makine için tüm uzantıları listeler.</span><span class="sxs-lookup"><span data-stu-id="d0c84-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="d0c84-112">Örnek 2: bir makinede belirli bir uzantı alma</span><span class="sxs-lookup"><span data-stu-id="d0c84-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="d0c84-113">Bir makinedeki belirli bir uzantıyı alır.</span><span class="sxs-lookup"><span data-stu-id="d0c84-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="d0c84-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0c84-114">PARAMETERS</span></span>

### <span data-ttu-id="d0c84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c84-115">-DefaultProfile</span></span>
<span data-ttu-id="d0c84-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0c84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c84-117">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="d0c84-117">-Expand</span></span>
<span data-ttu-id="d0c84-118">İşlemde uygulanacak genişletme ifadesi.</span><span class="sxs-lookup"><span data-stu-id="d0c84-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c84-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d0c84-119">-MachineName</span></span>
<span data-ttu-id="d0c84-120">Uzantıyı içeren makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="d0c84-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c84-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0c84-121">-Name</span></span>
<span data-ttu-id="d0c84-122">Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="d0c84-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="d0c84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c84-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0c84-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d0c84-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c84-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d0c84-125">-SubscriptionId</span></span>
<span data-ttu-id="d0c84-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d0c84-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0c84-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d0c84-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c84-128">CommonParameters</span></span>
<span data-ttu-id="d0c84-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0c84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c84-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d0c84-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c84-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0c84-131">INPUTS</span></span>

## <span data-ttu-id="d0c84-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0c84-132">OUTPUTS</span></span>

### <span data-ttu-id="d0c84-133">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d0c84-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d0c84-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0c84-134">NOTES</span></span>

<span data-ttu-id="d0c84-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d0c84-135">ALIASES</span></span>

## <span data-ttu-id="d0c84-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0c84-136">RELATED LINKS</span></span>

