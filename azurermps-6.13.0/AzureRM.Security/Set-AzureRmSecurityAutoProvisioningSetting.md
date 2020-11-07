---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762580"
---
# <span data-ttu-id="426de-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="426de-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="426de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="426de-102">SYNOPSIS</span></span>
<span data-ttu-id="426de-103">Güncelleştirme otomatik hazırlama ayarı</span><span class="sxs-lookup"><span data-stu-id="426de-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="426de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="426de-104">SYNTAX</span></span>

### <span data-ttu-id="426de-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="426de-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426de-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="426de-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426de-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="426de-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="426de-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="426de-108">DESCRIPTION</span></span>
<span data-ttu-id="426de-109">Aboneliğin otomatik hazırlama ayarlarını açar veya kapatır.</span><span class="sxs-lookup"><span data-stu-id="426de-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="426de-110">Otomatik sağlama ayarları, Azure Güvenlik Merkezi 'nin VM 'larınıza yüklenecek bir güvenlik Aracısı için otomatik olarak sağlaması gerekip gerekmediğine karar vermenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="426de-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="426de-111">Güvenlik Aracısı, güvenlik uyarıları oluşturmak ve VM 'nin güvenlik uyumluluğunu izlemek için VM 'inizi izler.</span><span class="sxs-lookup"><span data-stu-id="426de-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="426de-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="426de-112">EXAMPLES</span></span>

### <span data-ttu-id="426de-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="426de-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="426de-114">Aboneliğin otomatik hazırlama ayarını açar.</span><span class="sxs-lookup"><span data-stu-id="426de-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="426de-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="426de-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="426de-116">Aboneliğin otomatik hazırlama ayarını kapatır.</span><span class="sxs-lookup"><span data-stu-id="426de-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="426de-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="426de-117">PARAMETERS</span></span>

### <span data-ttu-id="426de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426de-118">-DefaultProfile</span></span>
<span data-ttu-id="426de-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="426de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426de-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="426de-120">-EnableAutoProvision</span></span>
<span data-ttu-id="426de-121">Otomatik sağlama.</span><span class="sxs-lookup"><span data-stu-id="426de-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426de-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="426de-122">-InputObject</span></span>
<span data-ttu-id="426de-123">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="426de-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426de-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="426de-124">-Name</span></span>
<span data-ttu-id="426de-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="426de-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426de-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="426de-126">-ResourceId</span></span>
<span data-ttu-id="426de-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="426de-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426de-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="426de-128">-Confirm</span></span>
<span data-ttu-id="426de-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="426de-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426de-130">-WhatIf</span></span>
<span data-ttu-id="426de-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="426de-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="426de-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="426de-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426de-133">CommonParameters</span></span>
<span data-ttu-id="426de-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="426de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426de-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426de-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="426de-136">INPUTS</span></span>

### <span data-ttu-id="426de-137">System. String</span><span class="sxs-lookup"><span data-stu-id="426de-137">System.String</span></span>
<span data-ttu-id="426de-138">System. Management. Automation. SwitchParameter Microsoft. Azure. Commands. Security. modeller. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="426de-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="426de-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="426de-139">OUTPUTS</span></span>

### <span data-ttu-id="426de-140">Microsoft. Azure. Commands. Security. model. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="426de-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="426de-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="426de-141">NOTES</span></span>

## <span data-ttu-id="426de-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="426de-142">RELATED LINKS</span></span>
