---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266360"
---
# <span data-ttu-id="7e959-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7e959-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7e959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e959-102">SYNOPSIS</span></span>
<span data-ttu-id="7e959-103">Güncelleştirme otomatik hazırlama ayarı</span><span class="sxs-lookup"><span data-stu-id="7e959-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="7e959-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e959-104">SYNTAX</span></span>

### <span data-ttu-id="7e959-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e959-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e959-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="7e959-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e959-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7e959-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e959-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e959-108">DESCRIPTION</span></span>
<span data-ttu-id="7e959-109">Aboneliğin otomatik hazırlama ayarlarını açar veya kapatır.</span><span class="sxs-lookup"><span data-stu-id="7e959-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="7e959-110">Otomatik sağlama ayarları, Azure Güvenlik Merkezi 'nin VM 'larınıza yüklenecek bir güvenlik Aracısı için otomatik olarak sağlaması gerekip gerekmediğine karar vermenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7e959-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="7e959-111">Güvenlik Aracısı, güvenlik uyarıları oluşturmak ve VM 'nin güvenlik uyumluluğunu izlemek için VM 'inizi izler.</span><span class="sxs-lookup"><span data-stu-id="7e959-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="7e959-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e959-112">EXAMPLES</span></span>

### <span data-ttu-id="7e959-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e959-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="7e959-114">Aboneliğin otomatik hazırlama ayarını açar.</span><span class="sxs-lookup"><span data-stu-id="7e959-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="7e959-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e959-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="7e959-116">Aboneliğin otomatik hazırlama ayarını kapatır.</span><span class="sxs-lookup"><span data-stu-id="7e959-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="7e959-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e959-117">PARAMETERS</span></span>

### <span data-ttu-id="7e959-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e959-118">-DefaultProfile</span></span>
<span data-ttu-id="7e959-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e959-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e959-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="7e959-120">-EnableAutoProvision</span></span>
<span data-ttu-id="7e959-121">Otomatik sağlama.</span><span class="sxs-lookup"><span data-stu-id="7e959-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e959-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e959-122">-InputObject</span></span>
<span data-ttu-id="7e959-123">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7e959-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e959-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e959-124">-Name</span></span>
<span data-ttu-id="7e959-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7e959-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e959-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7e959-126">-ResourceId</span></span>
<span data-ttu-id="7e959-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7e959-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e959-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e959-128">-Confirm</span></span>
<span data-ttu-id="7e959-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e959-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e959-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e959-130">-WhatIf</span></span>
<span data-ttu-id="7e959-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e959-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e959-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e959-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e959-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e959-133">CommonParameters</span></span>
<span data-ttu-id="7e959-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e959-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e959-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e959-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e959-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e959-136">INPUTS</span></span>

### <span data-ttu-id="7e959-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7e959-137">System.String</span></span>

### <span data-ttu-id="7e959-138">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7e959-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7e959-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e959-139">OUTPUTS</span></span>

### <span data-ttu-id="7e959-140">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7e959-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7e959-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e959-141">NOTES</span></span>

## <span data-ttu-id="7e959-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e959-142">RELATED LINKS</span></span>
