---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: d4741bc0456abfe99071f57d3224db8925bd1724
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759228"
---
# <span data-ttu-id="70952-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="70952-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="70952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70952-102">SYNOPSIS</span></span>
<span data-ttu-id="70952-103">Güncelleştirme otomatik hazırlama ayarı</span><span class="sxs-lookup"><span data-stu-id="70952-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="70952-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70952-104">SYNTAX</span></span>

### <span data-ttu-id="70952-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70952-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70952-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="70952-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70952-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="70952-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70952-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="70952-108">DESCRIPTION</span></span>
<span data-ttu-id="70952-109">Aboneliğin otomatik hazırlama ayarlarını açar veya kapatır.</span><span class="sxs-lookup"><span data-stu-id="70952-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="70952-110">Otomatik sağlama ayarları, Azure Güvenlik Merkezi 'nin VM 'larınıza yüklenecek bir güvenlik Aracısı için otomatik olarak sağlaması gerekip gerekmediğine karar vermenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="70952-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="70952-111">Güvenlik Aracısı, güvenlik uyarıları oluşturmak ve VM 'nin güvenlik uyumluluğunu izlemek için VM 'inizi izler.</span><span class="sxs-lookup"><span data-stu-id="70952-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="70952-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70952-112">EXAMPLES</span></span>

### <span data-ttu-id="70952-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70952-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="70952-114">Aboneliğin otomatik hazırlama ayarını açar.</span><span class="sxs-lookup"><span data-stu-id="70952-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="70952-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="70952-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="70952-116">Aboneliğin otomatik hazırlama ayarını kapatır.</span><span class="sxs-lookup"><span data-stu-id="70952-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="70952-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70952-117">PARAMETERS</span></span>

### <span data-ttu-id="70952-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70952-118">-DefaultProfile</span></span>
<span data-ttu-id="70952-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70952-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70952-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="70952-120">-EnableAutoProvision</span></span>
<span data-ttu-id="70952-121">Otomatik sağlama.</span><span class="sxs-lookup"><span data-stu-id="70952-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="70952-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70952-122">-InputObject</span></span>
<span data-ttu-id="70952-123">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="70952-123">Input Object.</span></span>

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

### <span data-ttu-id="70952-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="70952-124">-Name</span></span>
<span data-ttu-id="70952-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="70952-125">Resource name.</span></span>

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

### <span data-ttu-id="70952-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="70952-126">-ResourceId</span></span>
<span data-ttu-id="70952-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="70952-127">Resource ID.</span></span>

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

### <span data-ttu-id="70952-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="70952-128">-Confirm</span></span>
<span data-ttu-id="70952-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70952-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70952-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70952-130">-WhatIf</span></span>
<span data-ttu-id="70952-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70952-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70952-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70952-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70952-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70952-133">CommonParameters</span></span>
<span data-ttu-id="70952-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70952-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70952-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70952-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70952-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70952-136">INPUTS</span></span>

### <span data-ttu-id="70952-137">System. String</span><span class="sxs-lookup"><span data-stu-id="70952-137">System.String</span></span>

### <span data-ttu-id="70952-138">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="70952-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="70952-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70952-139">OUTPUTS</span></span>

### <span data-ttu-id="70952-140">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="70952-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="70952-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70952-141">NOTES</span></span>

## <span data-ttu-id="70952-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70952-142">RELATED LINKS</span></span>
