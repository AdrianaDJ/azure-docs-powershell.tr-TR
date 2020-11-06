---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591182"
---
# <span data-ttu-id="15d69-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="15d69-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="15d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d69-102">SYNOPSIS</span></span>
<span data-ttu-id="15d69-103">Otomasyon bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15d69-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15d69-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15d69-105">DESCRIPTION</span></span>
<span data-ttu-id="15d69-106">**Yeni-AzureRmAutomationConnection** cmdlet 'ı Azure Otomasyonu 'nda bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15d69-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="15d69-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15d69-107">EXAMPLES</span></span>

### <span data-ttu-id="15d69-108">Örnek 1: bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15d69-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="15d69-109">İlk komut, $FieldValue değişkenine alan değerlerinin karma tablosunu atar.</span><span class="sxs-lookup"><span data-stu-id="15d69-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="15d69-110">İkinci komut, AutomationAccount01 adlı Otomasyon hesabında Connection12 adlı bir Azure bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15d69-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="15d69-111">Komut $FieldValues 'daki bağlantı alanı değerlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="15d69-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="15d69-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15d69-112">PARAMETERS</span></span>

### <span data-ttu-id="15d69-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15d69-113">-AutomationAccountName</span></span>
<span data-ttu-id="15d69-114">Bu cmdlet 'in bağlantı oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="15d69-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="15d69-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="15d69-116">Anahtar/değer çiftlerini içeren karma tabloyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="15d69-117">Anahtarlar belirtilen bağlantı türü için bağlantı alanlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="15d69-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="15d69-118">Değerler, bağlantı örneği için her bir bağlantı alanının belirli değerlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="15d69-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d69-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="15d69-119">-ConnectionTypeName</span></span>
<span data-ttu-id="15d69-120">Bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d69-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="15d69-121">-Description</span></span>
<span data-ttu-id="15d69-122">Bağlantının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-122">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d69-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="15d69-123">-Name</span></span>
<span data-ttu-id="15d69-124">Bağlantı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-124">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d69-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d69-125">-ResourceGroupName</span></span>
<span data-ttu-id="15d69-126">Bu cmdlet 'in bağlantı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d69-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="15d69-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d69-127">-DefaultProfile</span></span>
<span data-ttu-id="15d69-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15d69-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d69-129">CommonParameters</span></span>
<span data-ttu-id="15d69-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15d69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d69-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d69-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d69-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15d69-132">INPUTS</span></span>

## <span data-ttu-id="15d69-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15d69-133">OUTPUTS</span></span>

### <span data-ttu-id="15d69-134">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="15d69-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="15d69-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15d69-135">NOTES</span></span>

## <span data-ttu-id="15d69-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15d69-136">RELATED LINKS</span></span>

[<span data-ttu-id="15d69-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="15d69-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="15d69-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="15d69-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


