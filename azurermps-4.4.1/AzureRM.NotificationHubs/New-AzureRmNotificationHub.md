---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587825"
---
# <span data-ttu-id="38efe-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="38efe-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="38efe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38efe-102">SYNOPSIS</span></span>
<span data-ttu-id="38efe-103">Bildirim Merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38efe-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38efe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38efe-104">SYNTAX</span></span>

### <span data-ttu-id="38efe-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="38efe-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38efe-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="38efe-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38efe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38efe-107">DESCRIPTION</span></span>
<span data-ttu-id="38efe-108">**Yeni-AzureRmNotificationHub** cmdlet 'i bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38efe-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="38efe-109">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38efe-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="38efe-110">Bildirim Hub 'ları kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="38efe-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="38efe-111">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir bildirim merkezi oluşturmak için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="38efe-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="38efe-112">**Notificationhubattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38efe-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="38efe-113">Bu özellik değerlerini, *Notificationhubobj* parametresi aracılığıyla yeni hub 'ınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38efe-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="38efe-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38efe-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="38efe-115">**New-AzureRmNotificationHub** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, Batı ABD veri merkezinde bulunan ContosoNotificationHub adlı bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38efe-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="38efe-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38efe-116">EXAMPLES</span></span>

### <span data-ttu-id="38efe-117">Örnek 1: bildirim merkezi oluşturma</span><span class="sxs-lookup"><span data-stu-id="38efe-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="38efe-118">Bu komut ContosoNamespace ad alanında bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38efe-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="38efe-119">Yeni hub ContosoNotificationsGroup atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="38efe-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="38efe-120">Hub için bir ad veya başka bir yapılandırma bilgisi belirtmeniz gerekmez; Bu bilgiler C:\Configurations\InternalHub.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="38efe-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="38efe-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38efe-121">PARAMETERS</span></span>

### <span data-ttu-id="38efe-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="38efe-122">-InputFile</span></span>
<span data-ttu-id="38efe-123">Yeni Bildirim Hub 'ının yapılandırma değerlerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="38efe-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="38efe-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="38efe-124">-Namespace</span></span>
<span data-ttu-id="38efe-125">Bildirim Hub 'ına atanacak ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="38efe-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="38efe-126">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="38efe-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="38efe-127">Bildirim hubları var olan bir ad alanına atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="38efe-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="38efe-128">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir ad alanı oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="38efe-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="38efe-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="38efe-129">-NotificationHubObj</span></span>
<span data-ttu-id="38efe-130">Yeni Hub için yapılandırma bilgilerini içeren **Notificationhubattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38efe-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="38efe-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38efe-131">-ResourceGroup</span></span>
<span data-ttu-id="38efe-132">Bildirim Hub 'ına atanacak kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="38efe-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="38efe-133">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="38efe-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="38efe-134">Var olan bir kaynak grubunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="38efe-134">You must use an existing resource group.</span></span>
<span data-ttu-id="38efe-135">**Yeni-AzureRmNotificationHub** cmdlet 'i yeni bir kaynak grubu oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="38efe-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="38efe-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="38efe-136">-Confirm</span></span>
<span data-ttu-id="38efe-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38efe-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38efe-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38efe-138">-WhatIf</span></span>
<span data-ttu-id="38efe-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38efe-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38efe-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38efe-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38efe-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38efe-141">-DefaultProfile</span></span>
<span data-ttu-id="38efe-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38efe-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38efe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38efe-143">CommonParameters</span></span>
<span data-ttu-id="38efe-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38efe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38efe-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38efe-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38efe-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38efe-146">INPUTS</span></span>

## <span data-ttu-id="38efe-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38efe-147">OUTPUTS</span></span>

### <span data-ttu-id="38efe-148">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="38efe-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="38efe-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38efe-149">NOTES</span></span>

## <span data-ttu-id="38efe-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38efe-150">RELATED LINKS</span></span>

[<span data-ttu-id="38efe-151">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="38efe-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="38efe-152">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="38efe-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="38efe-153">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="38efe-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


