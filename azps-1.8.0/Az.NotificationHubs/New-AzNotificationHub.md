---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 9c65ec6f4cf1a8b9c6a8e85b196d4b61b62df09a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759900"
---
# <span data-ttu-id="e9b64-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e9b64-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="e9b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9b64-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b64-103">Bildirim Merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9b64-103">Creates a notification hub.</span></span>

## <span data-ttu-id="e9b64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9b64-104">SYNTAX</span></span>

### <span data-ttu-id="e9b64-105">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="e9b64-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b64-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b64-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9b64-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b64-108">**Yeni-AzNotificationHub** cmdlet 'i bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9b64-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="e9b64-109">Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e9b64-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="e9b64-110">Bildirim Hub 'ları kabaca tek tek uygulamalara eşdeğerdir: uygulamalarınızdan her birinin kendi Bildirim Hub 'ı vardır.</span><span class="sxs-lookup"><span data-stu-id="e9b64-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="e9b64-111">**Yeni-AzNotificationHub** cmdlet 'i, yeni bir bildirim merkezi oluşturmak için iki yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e9b64-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="e9b64-112">**Notificationhubattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="e9b64-113">Bu özellik değerlerini, *Notificationhubobj* parametresi aracılığıyla yeni hub 'ınıza kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="e9b64-114">Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="e9b64-115">**New-AzNotificationHub** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, Batı US veri merkezinde bulunan ContosoNotificationHub adlı bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9b64-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="e9b64-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9b64-116">EXAMPLES</span></span>

### <span data-ttu-id="e9b64-117">Örnek 1: bildirim merkezi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9b64-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="e9b64-118">Bu komut ContosoNamespace ad alanında bir bildirim merkezi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9b64-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="e9b64-119">Yeni hub ContosoNotificationsGroup atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="e9b64-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="e9b64-120">Hub için bir ad veya başka bir yapılandırma bilgisi belirtmeniz gerekmez; Bu bilgiler C:\Configurations\InternalHub.jsgiriş dosyasından alınır.</span><span class="sxs-lookup"><span data-stu-id="e9b64-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="e9b64-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9b64-121">PARAMETERS</span></span>

### <span data-ttu-id="e9b64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b64-122">-DefaultProfile</span></span>
<span data-ttu-id="e9b64-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9b64-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9b64-124">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="e9b64-124">-InputFile</span></span>
<span data-ttu-id="e9b64-125">Yeni Bildirim Hub 'ının yapılandırma değerlerini içeren bir JSON dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9b64-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="e9b64-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9b64-126">-Namespace</span></span>
<span data-ttu-id="e9b64-127">Bildirim Hub 'ına atanacak ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9b64-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="e9b64-128">Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e9b64-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="e9b64-129">Bildirim hubları var olan bir ad alanına atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e9b64-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="e9b64-130">**Yeni-AzNotificationHub** cmdlet 'i yeni bir ad alanı oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="e9b64-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="e9b64-131">-NotificationHubObj</span></span>
<span data-ttu-id="e9b64-132">Yeni Hub için yapılandırma bilgilerini içeren **Notificationhubattributes** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9b64-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="e9b64-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9b64-133">-ResourceGroup</span></span>
<span data-ttu-id="e9b64-134">Bildirim Hub 'ına atanacak kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9b64-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="e9b64-135">Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.</span><span class="sxs-lookup"><span data-stu-id="e9b64-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="e9b64-136">Var olan bir kaynak grubunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="e9b64-136">You must use an existing resource group.</span></span>
<span data-ttu-id="e9b64-137">**Yeni-AzNotificationHub** cmdlet 'i yeni bir kaynak grubu oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="e9b64-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9b64-138">-Confirm</span></span>
<span data-ttu-id="e9b64-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9b64-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b64-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b64-140">-WhatIf</span></span>
<span data-ttu-id="e9b64-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9b64-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9b64-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9b64-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b64-143">CommonParameters</span></span>
<span data-ttu-id="e9b64-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9b64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b64-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b64-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9b64-146">INPUTS</span></span>

### <span data-ttu-id="e9b64-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e9b64-147">System.String</span></span>

## <span data-ttu-id="e9b64-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9b64-148">OUTPUTS</span></span>

### <span data-ttu-id="e9b64-149">Microsoft. Azure. Commands. Notificationhub. modeller. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e9b64-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="e9b64-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9b64-150">NOTES</span></span>

## <span data-ttu-id="e9b64-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9b64-151">RELATED LINKS</span></span>

[<span data-ttu-id="e9b64-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e9b64-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="e9b64-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e9b64-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="e9b64-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e9b64-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


