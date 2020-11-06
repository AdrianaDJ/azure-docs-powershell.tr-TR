---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594915"
---
# <span data-ttu-id="09da0-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="09da0-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="09da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09da0-102">SYNOPSIS</span></span>
<span data-ttu-id="09da0-103">Bildirim Hub 'ının özellik değerlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09da0-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09da0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09da0-104">SYNTAX</span></span>

### <span data-ttu-id="09da0-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="09da0-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09da0-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="09da0-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09da0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09da0-107">DESCRIPTION</span></span>
<span data-ttu-id="09da0-108">**Set-AzureRmNotificationHub** cmdlet 'i bir Bildirim Hub 'ının özellik değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="09da0-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="09da0-109">Bildirim Merkezi özellik değerini iki şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09da0-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="09da0-110">Bir tane için, **Notificationhubattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yeni hub 'ın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09da0-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="09da0-111">Bu, .NET Framework ile yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="09da0-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="09da0-112">Bu özellik değerlerini, *Notificationhubobj* parametresi aracılığıyla merkezinizi kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09da0-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="09da0-113">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09da0-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="09da0-114">JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır:</span><span class="sxs-lookup"><span data-stu-id="09da0-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="09da0-115">{</span><span class="sxs-lookup"><span data-stu-id="09da0-115">{</span></span>  
    <span data-ttu-id="09da0-116">"Ad": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="09da0-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="09da0-117">"Konum": "Batı ABD",</span><span class="sxs-lookup"><span data-stu-id="09da0-117">"Location": "West US",</span></span>  
<span data-ttu-id="09da0-118">}</span><span class="sxs-lookup"><span data-stu-id="09da0-118">}</span></span>

<span data-ttu-id="09da0-119">**Set-AzureRmNotificationHub** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği ContosoNotificationHub adındaki bir Bildirim Hub 'ının konum DEĞERINI Batı ABD olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09da0-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="09da0-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09da0-120">EXAMPLES</span></span>

### <span data-ttu-id="09da0-121">Örnek 1: Bildirim Hub 'ının özellik değerlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="09da0-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="09da0-122">Bu komut ContosoNamespace ad alanında bulunan bir Bildirim Hub 'ının özellik değerlerini değiştirir ve bu değeri ContosoNotificationsGroup kaynak grubuna atadı.</span><span class="sxs-lookup"><span data-stu-id="09da0-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="09da0-123">Özellik değerlerinin yanı sıra, değiştirilecek hub 'ın adı komutta belirtilmez.</span><span class="sxs-lookup"><span data-stu-id="09da0-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="09da0-124">Bunun yerine bu bilgiler C:\Configuration\Hubs.jsgiriş dosyasında yer alır.</span><span class="sxs-lookup"><span data-stu-id="09da0-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="09da0-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09da0-125">PARAMETERS</span></span>

### <span data-ttu-id="09da0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09da0-126">-DefaultProfile</span></span>
<span data-ttu-id="09da0-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="09da0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09da0-128">-Force</span><span class="sxs-lookup"><span data-stu-id="09da0-128">-Force</span></span>
<span data-ttu-id="09da0-129">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="09da0-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="09da0-130">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="09da0-130">-InputFile</span></span>
<span data-ttu-id="09da0-131">Bildirim Hub 'ının yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09da0-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da0-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09da0-132">-Namespace</span></span>
<span data-ttu-id="09da0-133">Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09da0-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="09da0-134">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="09da0-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09da0-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="09da0-135">-NotificationHubObj</span></span>
<span data-ttu-id="09da0-136">Bu cmdlet 'in değiştirdiği Hub için yapılandırma bilgilerini içeren **Notificationhubattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09da0-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da0-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09da0-137">-ResourceGroup</span></span>
<span data-ttu-id="09da0-138">Bildirim Hub 'ına atanmış kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="09da0-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="09da0-139">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="09da0-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09da0-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="09da0-140">-Confirm</span></span>
<span data-ttu-id="09da0-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09da0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09da0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09da0-142">-WhatIf</span></span>
<span data-ttu-id="09da0-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09da0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09da0-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09da0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09da0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09da0-145">CommonParameters</span></span>
<span data-ttu-id="09da0-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09da0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09da0-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09da0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09da0-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09da0-148">INPUTS</span></span>

### <span data-ttu-id="09da0-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="09da0-149">None</span></span>
<span data-ttu-id="09da0-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="09da0-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09da0-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09da0-151">OUTPUTS</span></span>

### <span data-ttu-id="09da0-152">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="09da0-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="09da0-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09da0-153">NOTES</span></span>

## <span data-ttu-id="09da0-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09da0-154">RELATED LINKS</span></span>

[<span data-ttu-id="09da0-155">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="09da0-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="09da0-156">Yeni-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="09da0-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="09da0-157">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="09da0-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)


