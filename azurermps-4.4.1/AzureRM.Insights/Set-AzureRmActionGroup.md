---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592620"
---
# <span data-ttu-id="2dade-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2dade-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="2dade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dade-102">SYNOPSIS</span></span>
<span data-ttu-id="2dade-103">Yeni bir eylem grubunu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2dade-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dade-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dade-104">SYNTAX</span></span>

### <span data-ttu-id="2dade-105">ByPropertyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2dade-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dade-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2dade-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dade-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2dade-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dade-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dade-108">DESCRIPTION</span></span>
<span data-ttu-id="2dade-109">**Set-AzureRmActionGroup** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="2dade-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="2dade-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dade-110">EXAMPLES</span></span>

### <span data-ttu-id="2dade-111">Örnek 1: eylem grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="2dade-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="2dade-112">İlk iki komut iki alıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2dade-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="2dade-113">Son komutu, iki alıcı dahil olmak üzere bir eylem grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2dade-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="2dade-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dade-114">PARAMETERS</span></span>

### <span data-ttu-id="2dade-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2dade-115">-Name</span></span>
<span data-ttu-id="2dade-116">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2dade-116">The name of the action group.</span></span>

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

### <span data-ttu-id="2dade-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="2dade-117">-ShortName</span></span>
<span data-ttu-id="2dade-118">Eylem grubunun kısa adı.</span><span class="sxs-lookup"><span data-stu-id="2dade-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="2dade-119">-Alıcı</span><span class="sxs-lookup"><span data-stu-id="2dade-119">-Receiver</span></span>
<span data-ttu-id="2dade-120">Eylem grubunun alıcıları listesi.</span><span class="sxs-lookup"><span data-stu-id="2dade-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="2dade-121">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="2dade-121">-DisableGroup</span></span>
<span data-ttu-id="2dade-122">Eylem grubunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2dade-122">Disables the action group.</span></span>

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

### <span data-ttu-id="2dade-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2dade-123">-Confirm</span></span>
<span data-ttu-id="2dade-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2dade-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dade-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dade-125">-DefaultProfile</span></span>
<span data-ttu-id="2dade-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2dade-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dade-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dade-127">-InputObject</span></span>
<span data-ttu-id="2dade-128">Eylem grubu kaynağı</span><span class="sxs-lookup"><span data-stu-id="2dade-128">The action group resource</span></span>

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

### <span data-ttu-id="2dade-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dade-129">-ResourceGroupName</span></span>
<span data-ttu-id="2dade-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2dade-130">The resource group name</span></span>

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

### <span data-ttu-id="2dade-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2dade-131">-ResourceId</span></span>
<span data-ttu-id="2dade-132">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2dade-132">The resource id</span></span>

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

### <span data-ttu-id="2dade-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2dade-133">-Tag</span></span>
<span data-ttu-id="2dade-134">Eylem grubu kaynağının etiketleri</span><span class="sxs-lookup"><span data-stu-id="2dade-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="2dade-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dade-135">-WhatIf</span></span>
<span data-ttu-id="2dade-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dade-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dade-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2dade-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dade-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dade-138">CommonParameters</span></span>
<span data-ttu-id="2dade-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dade-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dade-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dade-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dade-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dade-141">INPUTS</span></span>

## <span data-ttu-id="2dade-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dade-142">OUTPUTS</span></span>

### <span data-ttu-id="2dade-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2dade-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2dade-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dade-144">NOTES</span></span>

## <span data-ttu-id="2dade-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dade-145">RELATED LINKS</span></span>

<span data-ttu-id="2dade-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Yeni-Azurermactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="2dade-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
