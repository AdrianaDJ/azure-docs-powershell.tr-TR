---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276749"
---
# <span data-ttu-id="a69d9-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="a69d9-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="a69d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a69d9-103">Yeni bir makine kaydettirmek için API</span><span class="sxs-lookup"><span data-stu-id="a69d9-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="a69d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a69d9-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="a69d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a69d9-105">DESCRIPTION</span></span>
<span data-ttu-id="a69d9-106">Yeni bir makine kaydettirmek için API</span><span class="sxs-lookup"><span data-stu-id="a69d9-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="a69d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a69d9-107">EXAMPLES</span></span>

### <span data-ttu-id="a69d9-108">Örnek 1: bağlantılı makine olarak kullandığınız makine</span><span class="sxs-lookup"><span data-stu-id="a69d9-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="a69d9-109">Bağlı bir makine olarak kullandığınız makine.</span><span class="sxs-lookup"><span data-stu-id="a69d9-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="a69d9-110">Örnek 2: bağlı bir cihaz olarak uzak bir makine</span><span class="sxs-lookup"><span data-stu-id="a69d9-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="a69d9-111">Uzak bir makineyi PowerShell uzaktan iletişimi kullanan bağlı bir cihaz olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="a69d9-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="a69d9-112">Not: Şu anda yalnızca hedefin penceresi destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a69d9-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="a69d9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a69d9-113">PARAMETERS</span></span>

### <span data-ttu-id="a69d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69d9-114">-DefaultProfile</span></span>
<span data-ttu-id="a69d9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a69d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="a69d9-116">-Location</span></span>
<span data-ttu-id="a69d9-117">Oluşturulan ConnectedMachine için konum.</span><span class="sxs-lookup"><span data-stu-id="a69d9-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a69d9-118">-Name</span></span>
<span data-ttu-id="a69d9-119">Bu makine için kullanılacak ad.</span><span class="sxs-lookup"><span data-stu-id="a69d9-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="a69d9-120">Varsayılan olarak ana bilgisayar adı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a69d9-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="a69d9-121">-Proxy</span></span>
<span data-ttu-id="a69d9-122">Kullanılacak ara sunucunun URI 'SI</span><span class="sxs-lookup"><span data-stu-id="a69d9-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="a69d9-123">-PSSession</span></span>
<span data-ttu-id="a69d9-124">Belirtildiğinde, Azure 'a makinalar kullanan komut her Psoturumunda çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="a69d9-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="a69d9-125">Not: Bu, yalnızca Windows 'da çalışır.</span><span class="sxs-lookup"><span data-stu-id="a69d9-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="a69d9-127">Makineyi eklemek istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a69d9-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a69d9-128">-SubscriptionId</span></span>
<span data-ttu-id="a69d9-129">Makineyi eklemek istediğiniz aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a69d9-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a69d9-130">-Tag</span></span>
<span data-ttu-id="a69d9-131">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a69d9-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69d9-132">CommonParameters</span></span>
<span data-ttu-id="a69d9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a69d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69d9-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a69d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69d9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a69d9-135">INPUTS</span></span>

## <span data-ttu-id="a69d9-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a69d9-136">OUTPUTS</span></span>

## <span data-ttu-id="a69d9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a69d9-137">NOTES</span></span>

<span data-ttu-id="a69d9-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a69d9-138">ALIASES</span></span>

## <span data-ttu-id="a69d9-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a69d9-139">RELATED LINKS</span></span>

