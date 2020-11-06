---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589342"
---
# <span data-ttu-id="91a28-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="91a28-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="91a28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91a28-102">SYNOPSIS</span></span>
<span data-ttu-id="91a28-103">Güvenlik Uyarısı durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="91a28-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91a28-104">SYNTAX</span></span>

### <span data-ttu-id="91a28-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91a28-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91a28-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="91a28-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91a28-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="91a28-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91a28-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="91a28-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91a28-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="91a28-109">DESCRIPTION</span></span>
<span data-ttu-id="91a28-110">Güvenlik Uyarısı durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="91a28-110">Sets a security alert state.</span></span>

## <span data-ttu-id="91a28-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91a28-111">EXAMPLES</span></span>

### <span data-ttu-id="91a28-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91a28-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="91a28-113">Oluşan bir güvenlik uyarısını ayırıyor.</span><span class="sxs-lookup"><span data-stu-id="91a28-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="91a28-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91a28-114">PARAMETERS</span></span>

### <span data-ttu-id="91a28-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="91a28-115">-ActionType</span></span>
<span data-ttu-id="91a28-116">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="91a28-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a28-117">-DefaultProfile</span></span>
<span data-ttu-id="91a28-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91a28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91a28-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91a28-119">-InputObject</span></span>
<span data-ttu-id="91a28-120">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="91a28-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="91a28-121">-Location</span></span>
<span data-ttu-id="91a28-122">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="91a28-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="91a28-123">-Name</span></span>
<span data-ttu-id="91a28-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="91a28-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="91a28-125">-PassThru</span></span>
<span data-ttu-id="91a28-126">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="91a28-126">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a28-127">-ResourceGroupName</span></span>
<span data-ttu-id="91a28-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="91a28-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a28-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="91a28-129">-ResourceId</span></span>
<span data-ttu-id="91a28-130">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="91a28-130">Resource ID.</span></span>

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

### <span data-ttu-id="91a28-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="91a28-131">-Confirm</span></span>
<span data-ttu-id="91a28-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91a28-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a28-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a28-133">-WhatIf</span></span>
<span data-ttu-id="91a28-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91a28-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91a28-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91a28-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a28-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a28-136">CommonParameters</span></span>
<span data-ttu-id="91a28-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91a28-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a28-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a28-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a28-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91a28-139">INPUTS</span></span>

### <span data-ttu-id="91a28-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91a28-140">System.String</span></span>
<span data-ttu-id="91a28-141">Microsoft. Azure. Commands. Security. cmdlet. Alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="91a28-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="91a28-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91a28-142">OUTPUTS</span></span>

### <span data-ttu-id="91a28-143">Microsoft. Azure. Commands. Security. modeller. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="91a28-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="91a28-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91a28-144">NOTES</span></span>

## <span data-ttu-id="91a28-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91a28-145">RELATED LINKS</span></span>
