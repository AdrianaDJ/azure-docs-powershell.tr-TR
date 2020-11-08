---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266852"
---
# <span data-ttu-id="ff401-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ff401-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="ff401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff401-102">SYNOPSIS</span></span>
<span data-ttu-id="ff401-103">Yerleşik kavanu hizmete dağıtın.</span><span class="sxs-lookup"><span data-stu-id="ff401-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="ff401-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff401-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ff401-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff401-105">DESCRIPTION</span></span>
<span data-ttu-id="ff401-106">Yerleşik kavanu hizmete dağıtın.</span><span class="sxs-lookup"><span data-stu-id="ff401-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="ff401-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff401-107">EXAMPLES</span></span>

### <span data-ttu-id="ff401-108">Örnek 1: yerel derlenmiş jar 'yi ada göre hizmete dağıtın.</span><span class="sxs-lookup"><span data-stu-id="ff401-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="ff401-109">Yerel derlenmiş jar 'yi ada göre hizmete dağıtın.</span><span class="sxs-lookup"><span data-stu-id="ff401-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="ff401-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff401-110">PARAMETERS</span></span>

### <span data-ttu-id="ff401-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="ff401-111">-AsJob</span></span>
<span data-ttu-id="ff401-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="ff401-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ff401-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff401-113">-DefaultProfile</span></span>
<span data-ttu-id="ff401-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff401-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff401-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="ff401-115">-JarPath</span></span>
<span data-ttu-id="ff401-116">Jar 'in yolu dağıtımı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ff401-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="ff401-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff401-117">-Name</span></span>
<span data-ttu-id="ff401-118">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ff401-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff401-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff401-119">-NoWait</span></span>
<span data-ttu-id="ff401-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="ff401-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ff401-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff401-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff401-122">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ff401-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ff401-123">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff401-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff401-124">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="ff401-124">-ServiceName</span></span>
<span data-ttu-id="ff401-125">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ff401-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ff401-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ff401-126">-SubscriptionId</span></span>
<span data-ttu-id="ff401-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="ff401-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff401-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ff401-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff401-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff401-129">-Confirm</span></span>
<span data-ttu-id="ff401-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff401-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff401-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff401-131">-WhatIf</span></span>
<span data-ttu-id="ff401-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff401-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff401-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff401-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff401-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff401-134">CommonParameters</span></span>
<span data-ttu-id="ff401-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff401-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff401-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff401-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff401-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff401-137">INPUTS</span></span>

## <span data-ttu-id="ff401-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff401-138">OUTPUTS</span></span>

### <span data-ttu-id="ff401-139">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. Api20190501Preview. ıappresource</span><span class="sxs-lookup"><span data-stu-id="ff401-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="ff401-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff401-140">NOTES</span></span>

<span data-ttu-id="ff401-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ff401-141">ALIASES</span></span>

## <span data-ttu-id="ff401-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff401-142">RELATED LINKS</span></span>

