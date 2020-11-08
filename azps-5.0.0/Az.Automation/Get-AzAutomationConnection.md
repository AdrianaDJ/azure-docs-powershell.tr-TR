---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276137"
---
# <span data-ttu-id="51921-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51921-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="51921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51921-102">SYNOPSIS</span></span>
<span data-ttu-id="51921-103">Otomasyon bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="51921-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="51921-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51921-104">SYNTAX</span></span>

### <span data-ttu-id="51921-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51921-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51921-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="51921-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51921-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="51921-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51921-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51921-108">DESCRIPTION</span></span>
<span data-ttu-id="51921-109">**Get-AzAutomationConnection** cmdlet 'i, bir veya daha fazla Azure Automation bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="51921-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="51921-110">Varsayılan olarak, bu cmdlet tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="51921-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="51921-111">Belirli bir bağlantı almak için bağlantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="51921-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="51921-112">Belirli bir türdeki tüm bağlantıları almak için bağlantı türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="51921-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="51921-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51921-113">EXAMPLES</span></span>

### <span data-ttu-id="51921-114">Örnek 1: tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="51921-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="51921-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="51921-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="51921-116">Örnek 2: bir türdeki tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="51921-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="51921-117">Bu komut, Contoso17 adlı Otomasyon hesabındaki bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="51921-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="51921-118">Bu komut, SqlServer türünün bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="51921-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="51921-119">Örnek 3: bağlantı alma</span><span class="sxs-lookup"><span data-stu-id="51921-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="51921-120">Bu komut, ContosoConnection adlı bağlantı için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="51921-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="51921-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51921-121">PARAMETERS</span></span>

### <span data-ttu-id="51921-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="51921-122">-AutomationAccountName</span></span>
<span data-ttu-id="51921-123">Bu cmdlet 'in bağlantıları aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51921-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="51921-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="51921-124">-ConnectionTypeName</span></span>
<span data-ttu-id="51921-125">Bu cmdlet 'in bağlantıları aldığı bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51921-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51921-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51921-126">-DefaultProfile</span></span>
<span data-ttu-id="51921-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51921-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51921-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="51921-128">-Name</span></span>
<span data-ttu-id="51921-129">Bu cmdlet 'in aldığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51921-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51921-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51921-130">-ResourceGroupName</span></span>
<span data-ttu-id="51921-131">Bu cmdlet 'in bağlantıları aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51921-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="51921-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51921-132">CommonParameters</span></span>
<span data-ttu-id="51921-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51921-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51921-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51921-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51921-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51921-135">INPUTS</span></span>

### <span data-ttu-id="51921-136">System. String</span><span class="sxs-lookup"><span data-stu-id="51921-136">System.String</span></span>

## <span data-ttu-id="51921-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51921-137">OUTPUTS</span></span>

### <span data-ttu-id="51921-138">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="51921-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="51921-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51921-139">NOTES</span></span>

## <span data-ttu-id="51921-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51921-140">RELATED LINKS</span></span>

[<span data-ttu-id="51921-141">Yeni-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51921-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="51921-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="51921-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


