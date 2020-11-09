---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320018"
---
# <span data-ttu-id="1a53e-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="1a53e-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="1a53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a53e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a53e-103">Windows sanal masaüstü kayıt bilgilerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1a53e-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="1a53e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a53e-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a53e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a53e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a53e-106">Windows sanal masaüstü kayıt bilgilerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1a53e-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="1a53e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a53e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a53e-108">Örnek 1: Windows sanal masaüstü kayıt belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a53e-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="1a53e-109">Bu komut, bir konak havuzunda Windows sanal masaüstü kayıt belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a53e-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="1a53e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a53e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a53e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a53e-111">-DefaultProfile</span></span>
<span data-ttu-id="1a53e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a53e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a53e-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="1a53e-113">-ExpirationTime</span></span>
<span data-ttu-id="1a53e-114">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="1a53e-114">Expiration Time</span></span>

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

### <span data-ttu-id="1a53e-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="1a53e-115">-HostPoolName</span></span>
<span data-ttu-id="1a53e-116">Konak havuzu adı</span><span class="sxs-lookup"><span data-stu-id="1a53e-116">Host Pool Name</span></span>

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

### <span data-ttu-id="1a53e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a53e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a53e-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1a53e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1a53e-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1a53e-119">-SubscriptionId</span></span>
<span data-ttu-id="1a53e-120">Abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="1a53e-120">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a53e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a53e-121">-Confirm</span></span>
<span data-ttu-id="1a53e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a53e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a53e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a53e-123">-WhatIf</span></span>
<span data-ttu-id="1a53e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a53e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a53e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a53e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a53e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a53e-126">CommonParameters</span></span>
<span data-ttu-id="1a53e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a53e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a53e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1a53e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a53e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a53e-129">INPUTS</span></span>

## <span data-ttu-id="1a53e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a53e-130">OUTPUTS</span></span>

### <span data-ttu-id="1a53e-131">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıregistrationınfo</span><span class="sxs-lookup"><span data-stu-id="1a53e-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="1a53e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a53e-132">NOTES</span></span>

<span data-ttu-id="1a53e-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1a53e-133">ALIASES</span></span>

## <span data-ttu-id="1a53e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a53e-134">RELATED LINKS</span></span>

