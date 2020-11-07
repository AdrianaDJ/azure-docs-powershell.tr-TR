---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: 2b57d4d39ccce5b91a3dd8b34a42ec714b385a71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753279"
---
# <span data-ttu-id="cb8c3-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cb8c3-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="cb8c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8c3-103">Otomasyon bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="cb8c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb8c3-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8c3-106">**New-AzAutomationConnection** cmdlet 'ı Azure Otomasyonu 'nda bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="cb8c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8c3-108">Örnek 1: ConnectionTypeName = Azure için bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb8c3-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="cb8c3-109">İlk komut, $FieldValue değişkenine alan değerlerinin karma tablosunu atar.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="cb8c3-110">İkinci komut, AutomationAccount01 adlı Otomasyon hesabında Connection12 adlı bir Azure bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="cb8c3-111">Komut $FieldValues 'daki bağlantı alanı değerlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="cb8c3-112">Örnek 2: ConnectionTypeName = AzureServicePrincipal için bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb8c3-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="cb8c3-113">Bu komut, $RunAsAccountConnectionFieldValues ve ConnectionTypeName = AzureServicePrincipal kullanılarak AutomationAccount01 adlı Otomasyon hesabında Connection13 adlı bir Azure bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="cb8c3-114">Bu ConnectionTypeName = AzureServicePrincipal genellikle Azure farklı çalışma hesabı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="cb8c3-115">Örnek 3: ConnectionTypeName = AzureClassicCertificate için bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb8c3-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="cb8c3-116">Bu komut, $ClassicRunAsAccountConnectionFieldValues ve ConnectionTypeName = AzureClassicCertificate kullanılarak AutomationAccount01 adlı Otomasyon hesabında Connection14 adlı bir Azure bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="cb8c3-117">Bu ConnectionTypeName = AzureClassicCertificate genellikle Azure klasik farklı çalışma hesabı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="cb8c3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb8c3-118">PARAMETERS</span></span>

### <span data-ttu-id="cb8c3-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb8c3-119">-AutomationAccountName</span></span>
<span data-ttu-id="cb8c3-120">Bu cmdlet 'in bağlantı oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="cb8c3-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="cb8c3-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="cb8c3-122">Anahtar/değer çiftlerini içeren karma tabloyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="cb8c3-123">Anahtarlar belirtilen bağlantı türü için bağlantı alanlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="cb8c3-124">Değerler, bağlantı örneği için her bir bağlantı alanının belirli değerlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="cb8c3-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="cb8c3-125">-ConnectionTypeName</span></span>
<span data-ttu-id="cb8c3-126">Bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="cb8c3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8c3-127">-DefaultProfile</span></span>
<span data-ttu-id="cb8c3-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cb8c3-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb8c3-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cb8c3-129">-Description</span></span>
<span data-ttu-id="cb8c3-130">Bağlantının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="cb8c3-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb8c3-131">-Name</span></span>
<span data-ttu-id="cb8c3-132">Bağlantı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="cb8c3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb8c3-133">-ResourceGroupName</span></span>
<span data-ttu-id="cb8c3-134">Bu cmdlet 'in bağlantı oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="cb8c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8c3-135">CommonParameters</span></span>
<span data-ttu-id="cb8c3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb8c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8c3-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb8c3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8c3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb8c3-138">INPUTS</span></span>

### <span data-ttu-id="cb8c3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cb8c3-139">System.String</span></span>

### <span data-ttu-id="cb8c3-140">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="cb8c3-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="cb8c3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb8c3-141">OUTPUTS</span></span>

### <span data-ttu-id="cb8c3-142">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="cb8c3-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="cb8c3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb8c3-143">NOTES</span></span>

## <span data-ttu-id="cb8c3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb8c3-144">RELATED LINKS</span></span>

[<span data-ttu-id="cb8c3-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cb8c3-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="cb8c3-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cb8c3-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)

