---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278741"
---
# <span data-ttu-id="34fb7-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="34fb7-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="34fb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="34fb7-103">Bir karma makinenin model görünümü veya örnek görünümü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="34fb7-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="34fb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34fb7-104">SYNTAX</span></span>

### <span data-ttu-id="34fb7-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34fb7-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34fb7-106">Al</span><span class="sxs-lookup"><span data-stu-id="34fb7-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34fb7-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="34fb7-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="34fb7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="34fb7-109">Bir karma makinenin model görünümü veya örnek görünümü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="34fb7-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="34fb7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="34fb7-111">Örnek 1: bir abonelikteki tüm bağlı makineleri listeleme</span><span class="sxs-lookup"><span data-stu-id="34fb7-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="34fb7-112">Bir abonelikteki tüm bağlı makineleri listeler.</span><span class="sxs-lookup"><span data-stu-id="34fb7-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="34fb7-113">Abonelik belirtilmezse, abonelik geçerli Azure PowerShell içeriğinden kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34fb7-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="34fb7-114">Örnek 2: kaynak grubundaki tüm bağlı makineleri listeleme</span><span class="sxs-lookup"><span data-stu-id="34fb7-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="34fb7-115">Kaynak grubundaki tüm bağlı makineleri listeler.</span><span class="sxs-lookup"><span data-stu-id="34fb7-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="34fb7-116">Örnek 3: ada göre kaynak grubunda bağlı bir makine edinme</span><span class="sxs-lookup"><span data-stu-id="34fb7-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="34fb7-117">Kaynak grubunda ada göre bağlı bir makine edinin.</span><span class="sxs-lookup"><span data-stu-id="34fb7-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="34fb7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34fb7-118">PARAMETERS</span></span>

### <span data-ttu-id="34fb7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34fb7-119">-DefaultProfile</span></span>
<span data-ttu-id="34fb7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34fb7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34fb7-121">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="34fb7-121">-Expand</span></span>
<span data-ttu-id="34fb7-122">İşlemde uygulanacak genişletme ifadesi.</span><span class="sxs-lookup"><span data-stu-id="34fb7-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34fb7-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="34fb7-123">-Name</span></span>
<span data-ttu-id="34fb7-124">Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="34fb7-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="34fb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34fb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="34fb7-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34fb7-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="34fb7-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="34fb7-127">-SubscriptionId</span></span>
<span data-ttu-id="34fb7-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="34fb7-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="34fb7-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34fb7-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="34fb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fb7-130">CommonParameters</span></span>
<span data-ttu-id="34fb7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34fb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fb7-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34fb7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fb7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34fb7-133">INPUTS</span></span>

## <span data-ttu-id="34fb7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34fb7-134">OUTPUTS</span></span>

### <span data-ttu-id="34fb7-135">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="34fb7-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="34fb7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34fb7-136">NOTES</span></span>

<span data-ttu-id="34fb7-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="34fb7-137">ALIASES</span></span>

## <span data-ttu-id="34fb7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34fb7-138">RELATED LINKS</span></span>

