---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: a50716315796d46185b67099784bc550295231e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753828"
---
# <span data-ttu-id="a2d61-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a2d61-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="a2d61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d61-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d61-103">Azure Web App sertifika SSL bağlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="a2d61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2d61-104">SYNTAX</span></span>

### <span data-ttu-id="a2d61-105">S1</span><span class="sxs-lookup"><span data-stu-id="a2d61-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d61-106">S2</span><span class="sxs-lookup"><span data-stu-id="a2d61-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d61-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2d61-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d61-108">**Get-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) bağlaması alır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="a2d61-109">SSL bağlamaları, bir Web uygulamasını karşıya yüklenen sertifikayla ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="a2d61-110">Web Apps, birden çok sertifikaya bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="a2d61-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2d61-111">EXAMPLES</span></span>

### <span data-ttu-id="a2d61-112">Örnek 1: Web uygulaması için SSL bağlamaları alma</span><span class="sxs-lookup"><span data-stu-id="a2d61-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="a2d61-113">Bu komut, ContosoResourceGroup kaynak grubuyla ilişkilendirilmiş olan ContosoWebApp Web App 'in SSL bağlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="a2d61-114">Örnek 2: Web uygulaması için SSL bağlamaları almak üzere nesne başvurusu kullanma</span><span class="sxs-lookup"><span data-stu-id="a2d61-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="a2d61-115">Bu örnekteki komutlar, Web uygulamasının ContosoWebApp için SSL bağlamalarını de alır; Bununla birlikte, Web uygulaması adı ve ilişkili kaynak grubunun adı yerine bir nesne başvurusu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="a2d61-116">Bu nesne başvurusu, örnekte, ContosoWebApp adlı Web uygulamasına bir nesne başvurusu oluşturmak üzere **Get-AzWebApp** kullanan ilk komut tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2d61-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="a2d61-117">Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="a2d61-118">Bu değişken ve **Get-AzWebAppSSLBinding** cmdlet 'ı, SSL bağlarını almak için ikinci komut tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2d61-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="a2d61-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2d61-119">PARAMETERS</span></span>

### <span data-ttu-id="a2d61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d61-120">-DefaultProfile</span></span>
<span data-ttu-id="a2d61-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2d61-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d61-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2d61-122">-Name</span></span>
<span data-ttu-id="a2d61-123">SSL bağlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d61-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d61-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2d61-125">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="a2d61-126">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a2d61-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d61-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a2d61-127">-Slot</span></span>
<span data-ttu-id="a2d61-128">Web uygulaması dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="a2d61-129">Dağıtım yuvası almak için Get-AzWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2d61-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d61-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a2d61-130">-WebApp</span></span>
<span data-ttu-id="a2d61-131">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-131">Specifies a Web App.</span></span>
<span data-ttu-id="a2d61-132">Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2d61-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d61-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a2d61-133">-WebAppName</span></span>
<span data-ttu-id="a2d61-134">Bu cmdlet 'in SSL bağlarını aldığı Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d61-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="a2d61-135">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a2d61-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d61-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d61-136">CommonParameters</span></span>
<span data-ttu-id="a2d61-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2d61-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d61-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d61-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d61-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2d61-139">INPUTS</span></span>

### <span data-ttu-id="a2d61-140">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="a2d61-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a2d61-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2d61-141">OUTPUTS</span></span>

### <span data-ttu-id="a2d61-142">Microsoft. Azure. Management. Web sitesi. modeller. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="a2d61-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="a2d61-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2d61-143">NOTES</span></span>

## <span data-ttu-id="a2d61-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2d61-144">RELATED LINKS</span></span>

[<span data-ttu-id="a2d61-145">Yeni-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a2d61-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="a2d61-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a2d61-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="a2d61-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a2d61-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


