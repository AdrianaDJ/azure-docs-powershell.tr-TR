---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 57b810c448c739b6346a410284272e26b44d3aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588857"
---
# <span data-ttu-id="86c94-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="86c94-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="86c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c94-102">SYNOPSIS</span></span>
<span data-ttu-id="86c94-103">Bildirim Merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c94-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86c94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86c94-104">SYNTAX</span></span>

### <span data-ttu-id="86c94-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="86c94-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c94-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c94-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c94-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="86c94-107">DESCRIPTION</span></span>
<span data-ttu-id="86c94-108">**Yeni-AzureRmNotificationHub** cmdlet 'i bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c94-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="86c94-109">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="86c94-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="86c94-110">Bildirim Hub 'ları kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="86c94-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="86c94-111">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir bildirim merkezi oluşturmak için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="86c94-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="86c94-112">**Notificationhubattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86c94-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="86c94-113">Bu özellik değerlerini, *Notificationhubobj* parametresi aracılığıyla yeni hub 'ınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86c94-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="86c94-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86c94-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="86c94-115">**New-AzureRmNotificationHub** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, Batı ABD veri merkezinde bulunan ContosoNotificationHub adlı bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c94-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="86c94-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86c94-116">EXAMPLES</span></span>

### <span data-ttu-id="86c94-117">Örnek 1: bildirim merkezi oluşturma</span><span class="sxs-lookup"><span data-stu-id="86c94-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="86c94-118">Bu komut ContosoNamespace ad alanında bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c94-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="86c94-119">Yeni hub ContosoNotificationsGroup atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="86c94-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="86c94-120">Hub için bir ad veya başka bir yapılandırma bilgisi belirtmeniz gerekmez; Bu bilgiler C:\Configurations\InternalHub.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="86c94-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="86c94-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86c94-121">PARAMETERS</span></span>

### <span data-ttu-id="86c94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c94-122">-DefaultProfile</span></span>
<span data-ttu-id="86c94-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="86c94-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c94-124">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="86c94-124">-InputFile</span></span>
<span data-ttu-id="86c94-125">Yeni Bildirim Hub 'ının yapılandırma değerlerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="86c94-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="86c94-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86c94-126">-Namespace</span></span>
<span data-ttu-id="86c94-127">Bildirim Hub 'ına atanacak ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="86c94-127">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="86c94-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="86c94-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="86c94-129">Bildirim hubları var olan bir ad alanına atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="86c94-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="86c94-130">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir ad alanı oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="86c94-130">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="86c94-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="86c94-131">-NotificationHubObj</span></span>
<span data-ttu-id="86c94-132">Yeni Hub için yapılandırma bilgilerini içeren **Notificationhubattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86c94-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="86c94-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86c94-133">-ResourceGroup</span></span>
<span data-ttu-id="86c94-134">Bildirim Hub 'ına atanacak kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="86c94-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="86c94-135">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="86c94-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="86c94-136">Var olan bir kaynak grubunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="86c94-136">You must use an existing resource group.</span></span>
<span data-ttu-id="86c94-137">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir kaynak grubu oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="86c94-137">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="86c94-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="86c94-138">-Confirm</span></span>
<span data-ttu-id="86c94-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86c94-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c94-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c94-140">-WhatIf</span></span>
<span data-ttu-id="86c94-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86c94-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86c94-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86c94-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c94-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c94-143">CommonParameters</span></span>
<span data-ttu-id="86c94-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86c94-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c94-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c94-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c94-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86c94-146">INPUTS</span></span>

### <span data-ttu-id="86c94-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="86c94-147">None</span></span>
<span data-ttu-id="86c94-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="86c94-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86c94-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86c94-149">OUTPUTS</span></span>

### <span data-ttu-id="86c94-150">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="86c94-150">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="86c94-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86c94-151">NOTES</span></span>

## <span data-ttu-id="86c94-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86c94-152">RELATED LINKS</span></span>

[<span data-ttu-id="86c94-153">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="86c94-153">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="86c94-154">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="86c94-154">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="86c94-155">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="86c94-155">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


