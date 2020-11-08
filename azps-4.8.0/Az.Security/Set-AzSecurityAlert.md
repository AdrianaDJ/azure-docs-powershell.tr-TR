---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266366"
---
# <span data-ttu-id="bd6f7-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="bd6f7-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="bd6f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6f7-103">Güvenlik Uyarısı durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-103">Updates a security alert state.</span></span>

## <span data-ttu-id="bd6f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd6f7-104">SYNTAX</span></span>

### <span data-ttu-id="bd6f7-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd6f7-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6f7-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="bd6f7-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6f7-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bd6f7-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6f7-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="bd6f7-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6f7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd6f7-109">DESCRIPTION</span></span>
<span data-ttu-id="bd6f7-110">Güvenlik Uyarısı durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-110">Sets a security alert state.</span></span>

## <span data-ttu-id="bd6f7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd6f7-111">EXAMPLES</span></span>

### <span data-ttu-id="bd6f7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd6f7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="bd6f7-113">Oluşan bir güvenlik uyarısını ayırıyor.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="bd6f7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd6f7-114">PARAMETERS</span></span>

### <span data-ttu-id="bd6f7-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="bd6f7-115">-ActionType</span></span>
<span data-ttu-id="bd6f7-116">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6f7-117">-DefaultProfile</span></span>
<span data-ttu-id="bd6f7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd6f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd6f7-119">-InputObject</span></span>
<span data-ttu-id="bd6f7-120">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6f7-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="bd6f7-121">-Location</span></span>
<span data-ttu-id="bd6f7-122">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6f7-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd6f7-123">-Name</span></span>
<span data-ttu-id="bd6f7-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6f7-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bd6f7-125">-PassThru</span></span>
<span data-ttu-id="bd6f7-126">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="bd6f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd6f7-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6f7-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bd6f7-129">-ResourceId</span></span>
<span data-ttu-id="bd6f7-130">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-130">Resource ID.</span></span>

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

### <span data-ttu-id="bd6f7-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd6f7-131">-Confirm</span></span>
<span data-ttu-id="bd6f7-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd6f7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6f7-133">-WhatIf</span></span>
<span data-ttu-id="bd6f7-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd6f7-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd6f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6f7-136">CommonParameters</span></span>
<span data-ttu-id="bd6f7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6f7-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bd6f7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6f7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd6f7-139">INPUTS</span></span>

### <span data-ttu-id="bd6f7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bd6f7-140">System.String</span></span>

### <span data-ttu-id="bd6f7-141">Microsoft. Azure. Commands. Security. modeller. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="bd6f7-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="bd6f7-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd6f7-142">OUTPUTS</span></span>

### <span data-ttu-id="bd6f7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd6f7-143">System.Boolean</span></span>

## <span data-ttu-id="bd6f7-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd6f7-144">NOTES</span></span>

## <span data-ttu-id="bd6f7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd6f7-145">RELATED LINKS</span></span>
