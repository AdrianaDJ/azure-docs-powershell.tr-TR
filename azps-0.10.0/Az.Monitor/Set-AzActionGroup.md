---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: aad8ebb5b78163319ca0c6f56780bd0e336853f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935677"
---
# <span data-ttu-id="ef857-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ef857-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="ef857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef857-102">SYNOPSIS</span></span>
<span data-ttu-id="ef857-103">Yeni bir eylem grubunu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ef857-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="ef857-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef857-104">SYNTAX</span></span>

### <span data-ttu-id="ef857-105">ByPropertyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef857-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef857-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ef857-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef857-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef857-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef857-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef857-108">DESCRIPTION</span></span>
<span data-ttu-id="ef857-109">**Set-AzActionGroup** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="ef857-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="ef857-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef857-110">EXAMPLES</span></span>

### <span data-ttu-id="ef857-111">Örnek 1: eylem grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ef857-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="ef857-112">İlk iki komut iki alıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ef857-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="ef857-113">Son komutu, iki alıcı dahil olmak üzere bir eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ef857-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="ef857-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef857-114">PARAMETERS</span></span>

### <span data-ttu-id="ef857-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef857-115">-DefaultProfile</span></span>
<span data-ttu-id="ef857-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ef857-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef857-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="ef857-117">-DisableGroup</span></span>
<span data-ttu-id="ef857-118">Eylem grubunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ef857-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef857-119">-InputObject</span></span>
<span data-ttu-id="ef857-120">Eylem grubu kaynağı</span><span class="sxs-lookup"><span data-stu-id="ef857-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef857-121">-Name</span></span>
<span data-ttu-id="ef857-122">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef857-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-123">-Alıcı</span><span class="sxs-lookup"><span data-stu-id="ef857-123">-Receiver</span></span>
<span data-ttu-id="ef857-124">Eylem grubunun alıcıları listesi.</span><span class="sxs-lookup"><span data-stu-id="ef857-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef857-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef857-126">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="ef857-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ef857-127">-ResourceId</span></span>
<span data-ttu-id="ef857-128">Kaynak ı</span><span class="sxs-lookup"><span data-stu-id="ef857-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="ef857-129">-ShortName</span></span>
<span data-ttu-id="ef857-130">Eylem grubunun kısa adı.</span><span class="sxs-lookup"><span data-stu-id="ef857-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ef857-131">-Tag</span></span>
<span data-ttu-id="ef857-132">Eylem grubu kaynağının etiketleri</span><span class="sxs-lookup"><span data-stu-id="ef857-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef857-133">-Confirm</span></span>
<span data-ttu-id="ef857-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef857-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef857-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef857-135">-WhatIf</span></span>
<span data-ttu-id="ef857-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef857-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef857-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef857-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef857-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef857-138">CommonParameters</span></span>
<span data-ttu-id="ef857-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef857-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef857-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ef857-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef857-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef857-141">INPUTS</span></span>

### <span data-ttu-id="ef857-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ef857-142">System.String</span></span>

### <span data-ttu-id="ef857-143">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. cmdlet., Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ef857-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ef857-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef857-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ef857-145">System. Koleksiyonlar. Generic. IDictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7nk 7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85din</span><span class="sxs-lookup"><span data-stu-id="ef857-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef857-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="ef857-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="ef857-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef857-147">OUTPUTS</span></span>

### <span data-ttu-id="ef857-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="ef857-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="ef857-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef857-149">NOTES</span></span>

## <span data-ttu-id="ef857-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef857-150">RELATED LINKS</span></span>

<span data-ttu-id="ef857-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Yeni-Azactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="ef857-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>