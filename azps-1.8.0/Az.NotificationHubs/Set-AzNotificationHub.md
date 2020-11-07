---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: f59ac6a2e1431c3ba04ff0ac9cf9cafbfdfe367e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759882"
---
# <span data-ttu-id="7f2e0-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f2e0-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="7f2e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2e0-103">Bildirim Hub 'ının özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="7f2e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f2e0-104">SYNTAX</span></span>

### <span data-ttu-id="7f2e0-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="7f2e0-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2e0-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f2e0-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2e0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f2e0-107">DESCRIPTION</span></span>
<span data-ttu-id="7f2e0-108">**Set-AzNotificationHub** cmdlet 'i bir Bildirim Hub 'ının özellik değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="7f2e0-109">Bildirim Merkezi özellik değerini iki şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="7f2e0-110">Bir tane için, **Notificationhubattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yeni hub 'ın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="7f2e0-111">Bu, .NET Framework ile yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="7f2e0-112">Bu özellik değerlerini, *Notificationhubobj* parametresi aracılığıyla merkezinizi kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="7f2e0-113">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="7f2e0-114">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır: {</span><span class="sxs-lookup"><span data-stu-id="7f2e0-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="7f2e0-115">"Ad": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="7f2e0-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="7f2e0-116">"Konum": "Batı ABD",</span><span class="sxs-lookup"><span data-stu-id="7f2e0-116">"Location": "West US",</span></span>  
<span data-ttu-id="7f2e0-117">} **Set-AzNotificationHub** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği ContosoNotificationHub adındaki bir Bildirim Hub 'ının konum DEĞERINI Batı ABD 'ye ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="7f2e0-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f2e0-118">EXAMPLES</span></span>

### <span data-ttu-id="7f2e0-119">Örnek 1: Bildirim Hub 'ının özellik değerlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="7f2e0-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="7f2e0-120">Bu komut ContosoNamespace ad alanında bulunan bir Bildirim Hub 'ının özellik değerlerini değiştirir ve bu değeri ContosoNotificationsGroup kaynak grubuna atadı.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="7f2e0-121">Özellik değerlerinin yanı sıra, değiştirilecek hub 'ın adı komutta belirtilmez.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="7f2e0-122">Bunun yerine bu bilgiler C:\Configuration\Hubs.jsgiriş dosyasında yer alır.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="7f2e0-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f2e0-123">PARAMETERS</span></span>

### <span data-ttu-id="7f2e0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2e0-124">-DefaultProfile</span></span>
<span data-ttu-id="7f2e0-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f2e0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f2e0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7f2e0-126">-Force</span></span>
<span data-ttu-id="7f2e0-127">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f2e0-128">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="7f2e0-128">-InputFile</span></span>
<span data-ttu-id="7f2e0-129">Bildirim Hub 'ının yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e0-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f2e0-130">-Namespace</span></span>
<span data-ttu-id="7f2e0-131">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7f2e0-132">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e0-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="7f2e0-133">-NotificationHubObj</span></span>
<span data-ttu-id="7f2e0-134">Bu cmdlet 'in değiştirdiği Hub için yapılandırma bilgilerini içeren **Notificationhubattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e0-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f2e0-135">-ResourceGroup</span></span>
<span data-ttu-id="7f2e0-136">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="7f2e0-137">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2e0-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f2e0-138">-Confirm</span></span>
<span data-ttu-id="7f2e0-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2e0-140">-WhatIf</span></span>
<span data-ttu-id="7f2e0-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2e0-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2e0-143">CommonParameters</span></span>
<span data-ttu-id="7f2e0-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f2e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2e0-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2e0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2e0-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f2e0-146">INPUTS</span></span>

### <span data-ttu-id="7f2e0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7f2e0-147">System.String</span></span>

## <span data-ttu-id="7f2e0-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f2e0-148">OUTPUTS</span></span>

### <span data-ttu-id="7f2e0-149">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7f2e0-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="7f2e0-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f2e0-150">NOTES</span></span>

## <span data-ttu-id="7f2e0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f2e0-151">RELATED LINKS</span></span>

[<span data-ttu-id="7f2e0-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f2e0-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="7f2e0-153">Yeni-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f2e0-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="7f2e0-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f2e0-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

