---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109316"
---
# <span data-ttu-id="6319b-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="6319b-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="6319b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6319b-102">SYNOPSIS</span></span>
<span data-ttu-id="6319b-103">Özel bulutun yönetici kimlik bilgilerini listeleme</span><span class="sxs-lookup"><span data-stu-id="6319b-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="6319b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6319b-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6319b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6319b-105">DESCRIPTION</span></span>
<span data-ttu-id="6319b-106">Özel bulutun yönetici kimlik bilgilerini listeleme</span><span class="sxs-lookup"><span data-stu-id="6319b-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="6319b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6319b-107">EXAMPLES</span></span>

### <span data-ttu-id="6319b-108">Örnek 1: özel bulutun yönetici kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="6319b-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="6319b-109">Özel bulutun yönetici kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="6319b-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="6319b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6319b-110">PARAMETERS</span></span>

### <span data-ttu-id="6319b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6319b-111">-DefaultProfile</span></span>
<span data-ttu-id="6319b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6319b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6319b-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="6319b-113">-PrivateCloudName</span></span>
<span data-ttu-id="6319b-114">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="6319b-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="6319b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6319b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6319b-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6319b-116">The name of the resource group.</span></span>
<span data-ttu-id="6319b-117">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6319b-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6319b-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6319b-118">-SubscriptionId</span></span>
<span data-ttu-id="6319b-119">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6319b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6319b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6319b-120">-Confirm</span></span>
<span data-ttu-id="6319b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6319b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6319b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6319b-122">-WhatIf</span></span>
<span data-ttu-id="6319b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6319b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6319b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6319b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6319b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6319b-125">CommonParameters</span></span>
<span data-ttu-id="6319b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6319b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6319b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6319b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6319b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6319b-128">INPUTS</span></span>

## <span data-ttu-id="6319b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6319b-129">OUTPUTS</span></span>

### <span data-ttu-id="6319b-130">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıadmincredentials</span><span class="sxs-lookup"><span data-stu-id="6319b-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="6319b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6319b-131">NOTES</span></span>

<span data-ttu-id="6319b-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6319b-132">ALIASES</span></span>

## <span data-ttu-id="6319b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6319b-133">RELATED LINKS</span></span>

