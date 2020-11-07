---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938967"
---
# <span data-ttu-id="77fad-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="77fad-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="77fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fad-102">SYNOPSIS</span></span>
<span data-ttu-id="77fad-103">Yeni bir eylem grubunu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="77fad-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77fad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77fad-104">SYNTAX</span></span>

### <span data-ttu-id="77fad-105">ByPropertyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77fad-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fad-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="77fad-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fad-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="77fad-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77fad-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="77fad-108">DESCRIPTION</span></span>
<span data-ttu-id="77fad-109">**Set-AzureRmActionGroup** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="77fad-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="77fad-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77fad-110">EXAMPLES</span></span>

### <span data-ttu-id="77fad-111">Örnek 1: eylem grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="77fad-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="77fad-112">İlk iki komut iki alıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77fad-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="77fad-113">Son komutu, iki alıcı dahil olmak üzere bir eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77fad-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="77fad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77fad-114">PARAMETERS</span></span>

### <span data-ttu-id="77fad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fad-115">-DefaultProfile</span></span>
<span data-ttu-id="77fad-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="77fad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fad-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="77fad-117">-DisableGroup</span></span>
<span data-ttu-id="77fad-118">Eylem grubunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="77fad-118">Disables the action group.</span></span>

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

### <span data-ttu-id="77fad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77fad-119">-InputObject</span></span>
<span data-ttu-id="77fad-120">Grup kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="77fad-120">The action group resourc</span></span>

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

### <span data-ttu-id="77fad-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="77fad-121">-Name</span></span>
<span data-ttu-id="77fad-122">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="77fad-122">The name of the action group.</span></span>

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

### <span data-ttu-id="77fad-123">-Alıcı</span><span class="sxs-lookup"><span data-stu-id="77fad-123">-Receiver</span></span>
<span data-ttu-id="77fad-124">Eylem grubunun alıcıları listesi.</span><span class="sxs-lookup"><span data-stu-id="77fad-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="77fad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fad-125">-ResourceGroupName</span></span>
<span data-ttu-id="77fad-126">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="77fad-126">The resource group nam</span></span>

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

### <span data-ttu-id="77fad-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="77fad-127">-ResourceId</span></span>
<span data-ttu-id="77fad-128">Kaynak ı</span><span class="sxs-lookup"><span data-stu-id="77fad-128">The resource i</span></span>

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

### <span data-ttu-id="77fad-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="77fad-129">-ShortName</span></span>
<span data-ttu-id="77fad-130">Eylem grubunun kısa adı.</span><span class="sxs-lookup"><span data-stu-id="77fad-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="77fad-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="77fad-131">-Tag</span></span>
<span data-ttu-id="77fad-132">İşlem grubu</span><span class="sxs-lookup"><span data-stu-id="77fad-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="77fad-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="77fad-133">-Confirm</span></span>
<span data-ttu-id="77fad-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77fad-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77fad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77fad-135">-WhatIf</span></span>
<span data-ttu-id="77fad-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77fad-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77fad-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77fad-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77fad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fad-138">CommonParameters</span></span>
<span data-ttu-id="77fad-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77fad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fad-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77fad-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fad-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77fad-141">INPUTS</span></span>

### <span data-ttu-id="77fad-142">System. String</span><span class="sxs-lookup"><span data-stu-id="77fad-142">System.String</span></span>

### <span data-ttu-id="77fad-143">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77fad-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="77fad-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77fad-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="77fad-145">System. Koleksiyonlar. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="77fad-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="77fad-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="77fad-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="77fad-147">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77fad-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="77fad-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77fad-148">OUTPUTS</span></span>

### <span data-ttu-id="77fad-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="77fad-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="77fad-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77fad-150">NOTES</span></span>

## <span data-ttu-id="77fad-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77fad-151">RELATED LINKS</span></span>

<span data-ttu-id="77fad-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Yeni-Azurermactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="77fad-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
