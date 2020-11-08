---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105665"
---
# <span data-ttu-id="b857f-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="b857f-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="b857f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b857f-102">SYNOPSIS</span></span>
<span data-ttu-id="b857f-103">Uygulama ağ geçidi yapılandırma bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="b857f-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="b857f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b857f-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b857f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b857f-105">DESCRIPTION</span></span>
<span data-ttu-id="b857f-106">**Get-AzureApplicationGatewayConfig** cmdlet 'ı bir Azure Application Gateway yapılandırma bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="b857f-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="b857f-107">Bağlam hem yapılandırma nesnesini hem de XML yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="b857f-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="b857f-108">XML yapılandırmasını dosyaya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b857f-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="b857f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b857f-109">EXAMPLES</span></span>

### <span data-ttu-id="b857f-110">Örnek 1: uygulama ağ geçidi yapılandırmasını alma ve dosyaya kaydetme</span><span class="sxs-lookup"><span data-stu-id="b857f-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="b857f-111">Bu komut, ApplicationGateway06 adlı bir uygulama ağ geçidinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b857f-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="b857f-112">Komut dosyayı belirtilen yolda kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b857f-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="b857f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b857f-113">PARAMETERS</span></span>

### <span data-ttu-id="b857f-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="b857f-114">-ExportToFile</span></span>
<span data-ttu-id="b857f-115">Bu cmdlet 'in yapılandırmayı XML biçiminde kaydettiği bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b857f-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b857f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b857f-116">-Name</span></span>
<span data-ttu-id="b857f-117">Bu cmdlet 'in yapılandırma bilgilerini aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b857f-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b857f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b857f-118">-Profile</span></span>
<span data-ttu-id="b857f-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b857f-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b857f-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b857f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b857f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b857f-121">CommonParameters</span></span>
<span data-ttu-id="b857f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b857f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b857f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b857f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b857f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b857f-124">INPUTS</span></span>

### <span data-ttu-id="b857f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b857f-125">System.String</span></span>

## <span data-ttu-id="b857f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b857f-126">OUTPUTS</span></span>

### <span data-ttu-id="b857f-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="b857f-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="b857f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b857f-128">NOTES</span></span>

## <span data-ttu-id="b857f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b857f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b857f-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="b857f-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


