---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939026"
---
# <span data-ttu-id="230c2-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="230c2-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="230c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="230c2-102">SYNOPSIS</span></span>
<span data-ttu-id="230c2-103">Azure Web App sertifika SSL bağlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="230c2-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="230c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="230c2-104">SYNTAX</span></span>

### <span data-ttu-id="230c2-105">S1</span><span class="sxs-lookup"><span data-stu-id="230c2-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230c2-106">S2</span><span class="sxs-lookup"><span data-stu-id="230c2-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="230c2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="230c2-107">DESCRIPTION</span></span>
<span data-ttu-id="230c2-108">**Get-AzureRmWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) bağlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="230c2-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="230c2-109">SSL bağlamaları, bir Web uygulamasını karşıya yüklenen sertifikayla ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="230c2-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="230c2-110">Web Apps, birden çok sertifikaya bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="230c2-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="230c2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="230c2-111">EXAMPLES</span></span>

### <span data-ttu-id="230c2-112">Örnek 1: Web uygulaması için SSL bağlamaları alma</span><span class="sxs-lookup"><span data-stu-id="230c2-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="230c2-113">Bu komut, ContosoResourceGroup kaynak grubuyla ilişkilendirilmiş olan ContosoWebApp Web App 'in SSL bağlarını alır.</span><span class="sxs-lookup"><span data-stu-id="230c2-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="230c2-114">Örnek 2: Web uygulaması için SSL bağlamaları almak üzere nesne başvurusu kullanma</span><span class="sxs-lookup"><span data-stu-id="230c2-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="230c2-115">Bu örnekteki komutlar, Web uygulamasının ContosoWebApp için SSL bağlamalarını de alır; Bununla birlikte, Web uygulaması adı ve ilişkili kaynak grubunun adı yerine bir nesne başvurusu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="230c2-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="230c2-116">Bu nesne başvurusu, örnekte, ContosoWebApp adlı Web uygulamasına nesne başvurusu oluşturmak üzere **Get-AzureRmWebApp** kullanan ilk komut tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="230c2-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="230c2-117">Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="230c2-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="230c2-118">Bu değişken ve **Get-AzureRmWebAppSSLBinding** cmdlet 'ı, SSL bağlamalarını almak için ikinci komut tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="230c2-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="230c2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="230c2-119">PARAMETERS</span></span>

### <span data-ttu-id="230c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230c2-120">-DefaultProfile</span></span>
<span data-ttu-id="230c2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="230c2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="230c2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="230c2-122">-Name</span></span>
<span data-ttu-id="230c2-123">SSL bağlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="230c2-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="230c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="230c2-125">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="230c2-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="230c2-126">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="230c2-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="230c2-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="230c2-127">-Slot</span></span>
<span data-ttu-id="230c2-128">Web uygulaması dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="230c2-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="230c2-129">Dağıtım yuvası almak için Get-AzureRMWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="230c2-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="230c2-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="230c2-130">-WebApp</span></span>
<span data-ttu-id="230c2-131">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="230c2-131">Specifies a Web App.</span></span>
<span data-ttu-id="230c2-132">Web uygulaması edinmek için Get-AzureRmWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="230c2-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230c2-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="230c2-133">-WebAppName</span></span>
<span data-ttu-id="230c2-134">Bu cmdlet 'in SSL bağlarını aldığı Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="230c2-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="230c2-135">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="230c2-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="230c2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230c2-136">CommonParameters</span></span>
<span data-ttu-id="230c2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="230c2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230c2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230c2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230c2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="230c2-139">INPUTS</span></span>

### <span data-ttu-id="230c2-140">Bölge</span><span class="sxs-lookup"><span data-stu-id="230c2-140">Site</span></span>
<span data-ttu-id="230c2-141">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="230c2-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="230c2-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="230c2-142">OUTPUTS</span></span>

## <span data-ttu-id="230c2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="230c2-143">NOTES</span></span>

## <span data-ttu-id="230c2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="230c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="230c2-145">Yeni-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="230c2-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="230c2-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="230c2-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="230c2-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="230c2-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


